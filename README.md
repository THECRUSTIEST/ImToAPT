# ImToAPT
A simple python library for encoding images into APT signals.

## Usage
    import ImToAPT as APT
Convert any image (x<909):
    APT.iToSig(img, bitRate=44100)
Yields a Numpy array of shape (n,) 
Convert an already imported object to an APT signal
where img is a PIL image object or an RGBA Numpy array.
