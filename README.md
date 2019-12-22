# Libre1-NS

Upload data collected by the Libre1 reader to Nightscout

## Hardware

- Freestyle Libre reader (version 1) and USB cable
- A computer with an USB port, running a suitable OS, as detailed below.

## Software

- An OS unixoid enough to run GNU date, Python and Bash scripts (Linux suggested - MacOSX has a different `date` syntax and doesn't work)
- Some software to extract the readings from the reader - e.g., https://github.com/Flameeyes/glucometerutils (Python)

## Preparations

- Read the memory of the reader into `readout.csv` using `glucometerutils`. See their README.
  (A sample CSV file is provided as `sample.csv` for demonstration purposes.)
  
## Procedure

- Starting with the `readout.csv` file, execute `./libre2json` which will produce a `upload-sg.json` file.
- Inspect that file.
- Use a suitable tool to upload the JSON data. (`upload-data` has been derived from https://github.com/steve8x8/Contour-NS)

## Caveats

- COMPLETELY UNTESTED.
- This is purely experimental, and has been provided for educational purposes. (Don't flame me for my coding style.)
- MacOSX "El Capitan" is not suited to run this software (because of a different `date` implementation).
- Will not work with Libre 2 readers, or Libre 1 readers upgraded to the 2.4 software.
- See below.
- Oh, and I almost forgot: This is COMPLETELY UNTESTED!

# Disclaimer

Although I've been, and still am, successfully using this setup to upload my own recorded data to Nightscout,
your experience may be different. This is experimental, educational-only software. Use at your own risk!

Except that, the Nightscout disclaimer holds: Never ever make medical decisions based only on the data that
have been processed through this software. If in doubt, use an approved device - like your trusted BG meter.

For feedback, use the Issues.
