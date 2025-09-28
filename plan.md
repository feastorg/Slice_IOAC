# Rough Plan for SLC_IOAC

**Goal / Description:**

- Build a slice for **basic analog signal interfacing** and **lightweight mixed I/O** use.
- Provide protected **analog inputs/outputs** and some digital channels.
- Not a full DAQ, the focus is on **signal conditioning** and slow acquisition/control (future we will do Slice_DAQC).

**Design Plan:**

- 2–4 analog inputs with:
  - ±10 V range, resistor dividers, TVS, filtering
  - RC low-pass filters to clean signals
- 1–2 analog outputs:
  - Filtered PWM buffered via op-amp
  - Optional external DAC (SPI)
- 2 opto-isolated digital inputs
- 2 protected digital outputs (MOSFET or relay)

**Applications:**

- Reading analog sensors (e.g. potentiometers, 0–10 V)
- Generating analog control signals for drivers
- Small PID loops, voltage monitoring, signal interfacing
