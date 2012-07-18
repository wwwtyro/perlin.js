## perlin.js

A javascript 1, 2, and 3-dimensional perlin noise generator. Cobbled together
with Sean McCullough's port of Stefan Gustavson's java implementation of perlin
noise (https://gist.github.com/304522) and the Alea random number generator 
(http://baagoe.com/en/RandomMusings/javascript/).

### Usage

Create a perlin noise object:

    var pn = new Perlin('random seed');
    
The perlin noise object has one function, noise. It takes 3 arguments: an x, y, 
and z coordinate. If you fix one or two of these, the function will behave as 
a two or one-dimensional perlin noise function, respectively. For example:

    value = pn.noise(x, 0, 0); // Leave y and z fixed at zero while varying x will give you a 1D perlin noise function.
    
    value = pn.noise(x, y, 0); // Leave z fixed at zero while varying x and y will give you a 2D perlin noise function.
    
    value = pn.noise(x, y, z); // Varying x, y, and z will give you a 3D perlin noise function.
    
The noise function returns a value between 0 and 1. If the noise varies too 
rapidly in the interval you are calculating, you can scale the inputs 
accordingly:

    value = pn.noise(x/10, y/10, z/10);
    
This will slow the variance of the returned value by an order of magnitude.

### License

I don't believe in them. Do whatever you want with your bits.
