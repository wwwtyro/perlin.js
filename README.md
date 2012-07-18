### perlin.js

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
    
    
