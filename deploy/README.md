# Underdamped oscillation — interactive demo

Single-file HTML/canvas animation of a damped mass–spring system (ζ < 1).
No build step, no dependencies, no external requests.

## Panels

- **Mass–spring–damper rig** — animated mass on a spring with a dashpot, showing the
  restoring force F_s = −kx and damping force F_d = −bv as live vectors.
- **Displacement x(t)** — the decaying oscillation x = x₀e^(−γt)cos(ω_d t) with its
  envelope, successive peak markers and the measured peak ratio e^(−γT_d).
- **Energy budget** — potential, kinetic and total energy vs time, normalised to E₀,
  with the E₀e^(−2γt) guide and a live KE/PE bar.
- **Phase portrait** — x/x₀ against v/(ω₀x₀), spiralling into the origin.

## Controls

ζ, ω₀ and playback speed are adjustable; envelope, velocity and peak markers toggle.
Space pauses, R restarts.

## Readouts

γ, ω_d, T_d, Q = 1/(2ζ), logarithmic decrement δ = 2πζ/√(1−ζ²), E/E₀ and x/x₀.

## Notes

Time-series panels are dimensionless (m = 1, x₀ = 1). The analytic solution was
verified against an independent RK4 integration of ẍ = −2γẋ − ω₀²x, agreeing to
~1e-12; the plotted log decrement matches 2πζ/√(1−ζ²) to 5 decimals.
