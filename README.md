Download Link: https://assignmentchef.com/product/solved-cs2400-lab-7-computer-class
<br>
Classes, friend functions and overloaded operators.

<strong>Computer class: </strong>

Design a computer class (<em>Computer</em>) that describes a computer object. A computer has the following properties:

<ul>

 <li>Amount of Ram in GB (examples: 8, 16), defaults to 8.</li>

 <li>Hard drive size in GB (examples: 500, 1000), defaults to 500.</li>

 <li>Speed in GHz (examples: 1.6, 2.4), defaults to 1.6.</li>

 <li>Type (laptop, desktop), defaults to “desktop”</li>

</ul>

Provide the following functions for the class:

<ul>

 <li>A default constructor (constructor with no parameters) that initializes all the variables to their default values.</li>

 <li>A constructor with four parameters to initialize all four member variables.</li>

 <li>Getters(accessors) and setters(mutators) for all four member variables.</li>

 <li>Calculate the price using the following formulas:</li>

</ul>

o <strong>Laptop</strong>: 600.00 + amount of ram in GB * 5.00 + Hard drive size * .15


(speed in GHz – 1.6) * 200 o <strong>Desktop</strong>: 400.00 + amount of ram in GB * 4.00 + Hard drive size in GB * .10 + (speed in GHz – 1.6) * 200

<ul>

 <li>Overload the &lt;&lt; operator to output all properties of a computer.</li>

 <li>Overload the &gt;&gt; operator that reads all four properties of a computer.</li>

 <li>Overload the == operator test if two computers are the same (all properties must match)</li>

 <li>Overload the &lt; operator that compares the prices of two computers.</li>

</ul>

<strong>You don’t have to check for invalid values. </strong>

<strong>Test the Computer class with the following main program.  </strong>

int main()

{

Computer comp; //use default constructor  Computer comp1(16, 1000, 1.6, “Laptop”);

cout &lt;&lt; comp &lt;&lt; endl; //output defaults       cout &lt;&lt; endl;  cout &lt;&lt; comp1 &lt;&lt; endl;

cout &lt;&lt; endl;

comp1.setRam(32);

comp1.setHd(2000);

int compRam = comp1.getRam();

cout &lt;&lt; “The computer ram was changed to ”

&lt;&lt; comp1.getRam() &lt;&lt; endl;      cout &lt;&lt; “The computer hd was changed to ”

&lt;&lt; comp1.getHd() &lt;&lt; endl;  cout &lt;&lt; “Updated info” &lt;&lt; endl &lt;&lt; endl;

cout &lt;&lt; comp1 &lt;&lt; endl;     cout &lt;&lt; endl;  comp1.setType(“Desktop”);

cout &lt;&lt; “Computer type was changed to Desktop” &lt;&lt; endl;    cout &lt;&lt; comp1 &lt;&lt; endl;




Computer comp2;

cout &lt;&lt; “Enter specs of a computer (Ram, HD, Speed, Type)” &lt;&lt; endl;       cin &gt;&gt; comp2;  cout &lt;&lt; comp2 &lt;&lt; endl;

if (comp1 &lt; comp2)

{

cout &lt;&lt; “Computer 2 is more expensive” &lt;&lt; endl;

}

if (comp1 == comp2)

{

cout &lt;&lt; “comp1 and comp2 have the same specifications” &lt;&lt; endl;

}




return 0;

}


