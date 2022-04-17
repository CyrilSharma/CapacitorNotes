# Capacitors

### **Mechanics**

Capacitors are two conducting plates seperated by a short distance, filled with either air or some other material (known as the dielectric). 

![Capacitors%2074e81/1820724A-3C29-40C4-B808-7B66C2806359.jpeg](Capacitors%2074e81/1820724A-3C29-40C4-B808-7B66C2806359.jpeg)

Presume that the above is your circuit. Here's what'll happen when everything's hooked up and before the capacitors are charged. 

1. The top and bottom capacitor plates will become equipotential surfaces alongside their respective battery terminal and their wire.
2. The positive terminal will take electrons from the positive plate, since a positive electric potential means a buildup of positive charge which will attract electrons. 
3. Similarly, the negative terminal will donate electrons to the negative plate.
4. Now the capacitors are charged and there are now two distinct equipotential surfaces. 

Now assume the voltage drops.

1. Charge begins to flow again as the plates are at a different voltage than the terminals.
    - The postive plate now has a higher electric potential than the terminal meaning it starts to attract electrons more than the terminal. This causes a net flow of electrons towards the positive plate.
    - The negative plate has a lower electric potential than the terminal, resulting in a flow of electrons back towards the terminal.

<aside>
💡 In any capacitor, the charge buildup on either plate only stops when the net electric field is zero for charges on the plate. This occurs for a certain amount of charge build up, which depends on the electric field. Since the electric field is equally strong for both plates, the magnitude of charge build-up is the same on both plates. However, the electric field points into one and out of the other. Therefore, the charge build-up is equal and opposite on the plates in a capacitor.

</aside>

### **Derivation of Capacitance**

You can see that the amount of charge a plate holds is some function of the voltage. This is why capacitance is defined as the amount of charge held, per unit voltage.

To calculate the general expression for capacitance, calculate the voltage as a function of the plate seperation.

$$
\triangle V = \frac{qd}{A\epsilon_0}
$$

Re-arranging...

$$
q = \frac{A\epsilon_0 \triangle V}{d} \rightarrow C = \frac{A\epsilon_0}{d} \rightarrow q = C\triangle V
$$

Meaning that if voltage is held constant, area and distance will affect the stored charge as follows. Why is this equation reasonable? Note that this equation also implies the units of "the permitivvity of free space" (epsilon) are farads/meter. 

### **Series / Parallel**

First, let's look at capacitors in series. 

![Capacitors%2074e81/04229027-2AAF-4ABA-B807-09EBAB1C5E4E.jpeg](Capacitors%2074e81/04229027-2AAF-4ABA-B807-09EBAB1C5E4E.jpeg)

Assume the top plate (red) of the first capacitor charges to q. As shown previously, the charges on the plates of a capacitor are equal and and opposite in signs. Next, note that since the orange bit must be nuetral (it's not connected to anything that can give it charge) the charges across it must be equal and opposite in signs as well. Through this logic, you can deduce the charges on all of the plates are either + or - q. And now you can derive how capacitors work in series.

$$
q = c_1\triangle V_1 \hspace{0.3in} q = c_2\triangle V_2 \\[0.1in] \frac{q}{c_1} + \frac{q}{c_2} = \triangle V \rightarrow \frac{q}{c_1} + \frac{q}{c_2} = \frac{q}{c_{net}} \\[0.1in] C_{net} = \frac{1}{\frac{1}{c_1} + \frac{1}{c_2}}  
$$

In parallel, each capacitor goes through an equal voltage drop and through a similar, but much simpler, logic it can be shown that the total capacitance is the sum of the individual capacitance.

### **Energy Storage**

Suppose some charge q' has already been transferred from one plate to another. The potential difference between the plates is:

$$
\triangle V' = q'/C
$$

Now suppose some tiny charge dq is transferred. This tiny charge dq will have almost no effect on the voltage and thus we can use the voltage to compute how much energy this particle transferred. The change in the potential energy is as follows:

$$
dU = \triangle V'dq = \frac{q'}{C}dq
$$

Now if you continue this process, allowing a total of q charge to pass, you'll get this expression:

$$
U = \int_{0}^{q}dU = \int_{0}^{q}\frac{q}{C}dq = \frac{q^2}{2C} 
$$

Or if you substitute q = C * delta(V)...

$$
U = \frac{1}{2} C\triangle V^2
$$

This energy is a distance dependent property, if you double the plate seperation the stored energy increases for the same reasons that it increases for two charged particles, it takes work to move oppositely charged particles apart. Note that if you double the distance, no other properties of the capacitor have changed to accomodate this energy. Thus, if the energy is not stored in a capacitor's plates, it must be stored between the plates in the form of the electric field.

Because energy is stored in the electric field, a 3D volume, it's useful to define an energy density caused by the electric field.

$$
u = \frac{U}{Volume} = \frac{\frac{1}{2} C\triangle V^2}{Ad} \rightarrow \frac{\frac{1}{2} \frac{A\epsilon_0}{d} \triangle V^2}{Ad} \rightarrow u = \frac{1}{2}\epsilon_0(\frac{\triangle V}{d})^2 \rightarrow \frac{1}{2}\epsilon_0 E^2 
$$

### Dielectrics

Dielectrics have some counter-intuitive effects in capacitance. Let’s start with how they affect capacitance when they're inserted into a charged capacitor not connected to a battery.

The dielectric will become polarized by the field of the capacitor causing the net electric field through the capacitor to be:

$$
E = \frac{E_0}{k}
$$

This reduces the voltage drop between the plates of the capacitor, and the charge must remain constant because it has nowhere to go, thus the capacitor holds the same amount of charge with 1/k times the voltage, increasing its capacitance by a factor of k.

The second scenario to consider is when a dieletric is inserted into a capacitor connected to a battery. Now, when the dielectric is inserted into the capacitor the electric field weakens, and so does the voltage across the capacitor because the net charge on either plate is q / k. However, since the plate is at a lower potential than the battery terminal, there must be a net flow of positive charge from the battery to the capacitor. This continues until the capacitor's plate is at the same potential as the battery terminal, which occurs when the net charge on the capacitor returns to it's initial charge q. Since the net charge on the plate is q / k, the capacitor's platemust charge up to k*q to reach this point, meaning the capacitance one again increases by a factor of k.

As a final example, imagine that you calculate the energy of the capacitor before and after the first example. You'll see that the energy of the capacitor must have decreased. Where did that energy go? Well whatever inserted the block took it out of the system. Left to itself the dielectric would be attracted to the capacitor, overshoot the center, and then lose its speed as it exited the capacitor. SHM
