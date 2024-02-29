# Fitting parabolas and other conic sections to a set of points

William Henney -  DAWGI Meeting - 2024-02-28

## Animation ##
![Animated GIF of presentation](presentation/dawgi-conics-talk.gif)

## Individual slides ##

### Title page ###
Fitting conic sections to data: Parabolae, ellipses, and hyperbolae
![001](slides/001.jpeg)

### What? ###
![002](slides/002.jpeg)

### From image … to points … to fitted curve ###
I can give another talk later on Stage 1
![003](slides/003.jpeg)

### Why? ###
![004](slides/004.jpeg)

### Curved emission arcs in H II regions ###
![005](slides/005.jpeg)

### Also in infrared … ###
And radio wavelengths too
![006](slides/006.jpeg)

### … and not just in Orion ###
![007](slides/007.jpeg)

### By fitting a conic section, we can measure ###
For instance, we may wish to know the orientation in order to identify the exciting source, or to compare with the magnetic field direction, etc
![008](slides/008.jpeg)

### But what if the shape is not a conic section? ###
![009](slides/009.jpeg)

### How? ###
![010](slides/010.jpeg)

### Algebraic distance versus geometric distance ###
![011](slides/011.jpeg)

### Disadvantages of algebraic distance ###
No clear intuitive interpretation of A, B, C, etc
![012](slides/012.jpeg)

### Geometric Euclidean distance ###
![013](slides/013.jpeg)

### Yes there is a simpler way ###
![014](slides/014.jpeg)

### This can be generalized to other forms of conics ###
Focal radius r and directrix distance d are trivial to calculatek
![015](slides/015.jpeg)

### If this is so clever, why did nobody else do it? ###
![016](slides/016.jpeg)

### Implementation: my confit python package ###
lmfit is for when astropy.modeling isn’t enough

The objective function calculates a vector of residuals, for which the
Minimizer tries to minimize the sum of squares

By default it uses a Levenberg-Marquardt algorithm
![017](slides/017.jpeg)

### Examples ###
![018](slides/018.jpeg)

### A simple curve with 7 points ###
![019](slides/01 9.jpeg)

### General conic versus parabola ###
![020](slides/002.jpeg)

### Unwanted spurious solutions ###
![021](slides/021.jpeg)

### Back to normal! ###
![022](slides/022.jpeg)

### With freely varying eccentricity we still have issues ###
This is a case where the covariance matrix underestimates the true
uncertainties

Better to use a parabola when the number of data points is small
![023](slides/023.jpeg)

### Test on real data ###
![024](slides/024.jpeg)

### A success ###
![025](slides/025.jpeg)

### But some edge cases still need to be finessed ###
![026](slides/026.jpeg)

### Conclusions ###
![027](slides/027.jpeg)

### Fitting conic sections can be useful, easy, and fun ###
![028](slides/028.jpeg)


# Abstract
## Fitting parabolas and other conic sections to a set of points

I will demonstrate a method for finding the orientation of the symmetry axis of an observed bow shock or other curved emission arc. The method consists in fitting a parabola (or ellipse, or hyperbola) to a set of points. A simple trick allows a suitable objective function to be defined without needing to explicitly calculate the distance of the points from the curve. The objective function can be minimized to find the best-fit conic section, and MCMC can be used to check for the presence of multiple local minima. 

## Ajuste de parábolas y otras secciones cónicas a un conjunto de puntos

Voy a demostrar un método para encontrar la orientación del eje de simetría de un arco de emisión observado. El método consiste en ajustar una parábola (o elipse, o hipérbola) a un conjunto de puntos. Un truco simple permite definir una función objetivo adecuada sin necesidad de calcular explícitamente la distancia de los puntos a la curva. La función objetivo se puede minimizar para encontrar la mejor sección cónica de ajuste, y MCMC se puede utilizar para comprobar la presencia de múltiples mínimos locales.


