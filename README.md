# ImToAPT
A simple python library for encoding images into APT signals.

## Usage
    import ImToAPT as APT
#### Convert any image (x<909):

    sig = APT.iToSig('img.png', sRate=44100, mod=1)

Yields a signal object which is a 2400 Hz carrier amplitude-modulated by image. Includes sync markers and pre-scan white/black space per APT standard. `mod` sets the modulation percentage (0-1). Default is 100% modulation (1) because moduation <100% requires normalization after signal reception.

#### Convert an already imported object to an APT signal:

    sig = APT.aToSig(img, sRate=44100, mod=1)
    
where img is a PIL image object or an RGBA or 2D Numpy array.

#### Export a signal to file:
    sig.export('out.wav')

Signal is exported to a .wav file. Filename, of course, can be changed to whatever you like.

# Prerequisites

* Numpy
* Scipy
* PIL (Pillow in Python 3.0 and above)
