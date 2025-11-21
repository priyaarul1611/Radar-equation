# Radar-Range using scilab

**AIM:**

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.

**Theory:**

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

**Formula**

<img width="400" height="500" alt="image" src="https://github.com/user-attachments/assets/51129076-a796-4121-acad-0255c725b717" />

Procedure:

1.Start the program.

2.Define constants such as the speed of light and the value of pi.

3.Input all radar parameters — these include the transmitted power, antenna gain, wavelength, radar cross-section, and the minimum detectable power.

4.Assign a fixed wavelength value directly (do not calculate it).

5.Substitute all known values of transmitted power, antenna gain, wavelength, radar cross-section, and minimum detectable power into the radar range equation.

6.Perform the necessary mathematical operations in Scilab to compute the maximum radar detection range.

7.Display the computed range on the screen in meters.

8.End the program.

**program:**
```
Pt = 1000;
G = 1000;
sigma = 1;
Ae = 10;

Smin = logspace(-12, -6, 100);
Rmax = ((Pt * G * sigma * Ae) ./ (16 * %pi^2 .* Smin)).^(1/4);
subplot(3,1,1);
plot(Smin, Rmax);

Ppeak = linspace(100, 10000, 100);
Rmax2 = ((Ppeak * G * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,2);
plot(Ppeak, Rmax2);

Gt = linspace(100, 2000, 100);
Rmax3 = ((Pt * Gt * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,3);
plot(Gt, Rmax3);
```
**output:**

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/363dea2b-9662-4d09-9eb1-9f508b9dcf38" />

**Tabulation:**


**Result:**
Thus, the maximum range of a radar system using the Radar Range Equation is verified using scilab

