# pm6665-reference-upgrade
Improved 10MHz oscillator for the PM6665 frequency counter.

The basic version of the PM6665 has a tunable Pierce oscillator with a 74HCU04.  
20 years later and with a **€5 budget**, we can do much better than that.  
The [hardware](../../wiki/BRD161205 R0) uses a VCTCXO with a **frequency stability of 500ppb** over the -40°C..85°C range.  The potmeter allows to calibrate for the initial 2ppm frequency offset of the oscillator.  

# Calibration
* For calibrating you'll need a frequency source that is even better than this oscillator.  Preferably, that reference is also cheap.  The **GPSDO** (GPS disciplined oscillator) is a widely used solution.  If you want it cheaper (and with less accuracy), you can take the 1PPS output of a Quectel L86-M33 GPS module.  This 1Hz pulse has a < 15ns accuracy, which is 15ppb.  
* **Yearly calibration** is needed, because the frequency of the VCTCXO will drift away by 1ppm/year.
