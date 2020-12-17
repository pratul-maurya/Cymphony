# Cymphony
An audio steganography project

A python script to hide text over an audio file in .wav format using LSB method. The main feature of this project is that this script does not distorts the sound of the carrier file. Also the output file is exactly the same size as the original carrier sound.

->Overview
  The script wav-steg.py is used to hide and recover secret message from the audio file. The input and output filenames for the secret text files are all configurable through    command line.
  The receiver must know the number of LSBs used and the number of bytes hidden in oreder to recover the data.
  
Command to hide data-
  python wav-steg.py --hide --data secret_file.txt --sound public_carrier_sound_2.wav --output steg_output.wav --nlsb 2

Command to recover data-
  python wav-steg.py --recover --sound steg_output.wav --output rec_secret_file.txt --nlsb 2 --bytes 444
