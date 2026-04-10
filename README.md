# Image Encrypt Decrypt v1.0 - By Sanjay Anoop Nair

Small tool for applying a rudimentary encryption / decryption on an image file. 

## What is this?
Image Encrypt Decrypt is a small tool for applying a rudimentary encryption / decryption on an image file. You can use it to encrypt an image using a string as a password, and later decrypt it using the same password at a later date.

## Why was this made?
This tool was made as I was interested in having a local implementation of an encryption / decryption tool as seen on various websites, so that it can be run on a mobile device.

## How does it work?
The logic used is an implementation similar to most sites offering similar tools, the password string is first hashed using `cyrb128` to give a 128-bit seed to a pseudorandom generator using `mulberry32`. The values generated are XORed with the pixels of the image to create the result. Since the process is symmetric, encryption and decryption are effectively the same operation.
