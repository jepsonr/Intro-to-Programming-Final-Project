#Final Project 
##Intro to Programming with C++
###Optimization of Marginal Profit (mill operations)
#### Genesis of the Project
The newly promoted general manager of a local iron mill faced several challeges when the previous manager quit:
  1. The flotation tank damage from overload
  2. The EPA injunctions for excessive moisture content in the tailings
  3. The SAG mill damage from improper feed rates of grinding material, raw ore, and water
  4. Meeting different market demands (foreign and domestic markets)
  5. Relying on density samples as a management tool indcuces significant lag-time 
  6. New (and current) employees needed more advanced skills in physics and math
The GM wanted a realtime management tool for plant operations

####Possible solutions a real time management tool:  
  1. One solution: install sensors costing as much as $50 million dollars in time and equipment
  2. A second solution: develop a mathematical model and statistical analysis tool

####Road blocks
  1. The mine was already in financial hardship, so installing sensors was not possible
  2. In the local mining culture, experience is valued over education, so highering a mining engineer was unlikely to happen
  
####The compromise
The mine decided they needed a three stage program for their employees. They sponsored their GM to meet with me to see if the college could meet their needs. The first stage was for me to help the GM with the physics and mathematical requirements of his job first. The second stage was for to develop a basic math and science course for all employees. The third stage was the development of a intermediate and advanced Mining Math and Science courses for supervisors and managers. Three weeks after the funding was approved, the mine had a catastrophic shut down and never recovered.

####The result
I visited the mine several times so that the GM could to familiarize me with the mill's design and systems. The GM came to the college several times for his math and science training. Within these few meetings we developed an outline and curriculum for the courses. I started developing the mathematical models and analysis tools for the mill operations. When it all came to a hault, I shelved the project, but in the back of my mind I kept thinking. This cannot be the only mine in the world that has these challenges and if someone could create a program to do what we started it could be marketable software. A year later I started studying computer programming it made sense to start creating the software myself.

####Current status and future possibilities
My Final Project for Introduction to Programming with C++ are two programs which complete the first two parts of the management tool we were developing. There are still 3 more parts to the management tool left. Each would take additional collaboration with a General Manager, but the basic formulas for part three are written. Part four was a long term data collection process that would lead to predictive and planning software. The last part would have been to create a generalized profit equation. The derivative of that equation could be used to manage feed rates and processing speeds that would maximize profits (marginal profit).

###Questions and inquiries for Phase 3: 
  1. What are the dimensions of P∙s  (percent of dry solids in the liquid times Specific gravity of the slurry)?
   	1. P∙s = %∙g/ml =  the volume of dry solids which requires the known G of the dry solids.
  	2. This raises a follow on question: 
  	3. Isn’t the G of the underflow that doesn’t pass through the shaker screenlower than the G that does pass? 
  	4. Or, is it simply the size of the chunck not the consistency of iron in the chunck?
  	5. More importantly, does it matter since the material not passing returns to the SAG mill?
  2. What are the dimensions of G (specific gravity of the dry solids)?
  	=grams/ml
  3. Can the G be calculated mathematically without using a Marcy scale?
  4. Can s.g. be calculated using P and s?
  5. Does the system of equations for slurry flow work? 
  6. Can the dilution ratio D be used as a coefficient for the system of equations?
  7. Could a combination of ρ,G,s,P be used in a system of equations that would yield the same flow rates?
  8. Can the values ρ,G,s,P,D be estimated or calculated (based on the ratio of low and high grade crushed ore and feed rates  of water at various stages of refinement)?
  9. Why does P change between the SAG Mill discharge and the SAG Cyclone Feed (approximately from 70% to 55%)?
  	Assumptions: Additional water dilution. Two sumps feed into the shaker screen, new water goes to SAG Mill.
  10. Where does sump water come from?
  	Assumptions: reclaimed from drying process.
  11. What is the Vp (Volumetric Loading =? % of total volume [total volume of what, the mill?]) which is the variable for the circulating load calculation.
  12. Is the SAG Mill discharge the same as the slurry going into the SAG Mill Discharge Pumpbox?
  	= yes
  14. Does the equation  PsubF∙GsubF=PsubU∙GsubU+PsubB∙GsubB hold.
  
  Common conversion ratios, approximate values and formulas:
  1. T=Short tons∙volumetric loading
  2. Tm=tons per volume of a mill
  3. V=volume   
  4. D=Diameter
  5. w=mass of the slurry in 〖ft〗^3  
  6. L=length of mill  
  7.  w=(weight of slurry in lbs)/〖ft〗^3 
  8. kwr=power draw in kilowatts (rod mill)
  9. Cs=Critical speed of a mill in rpm
  10. %Cs=Actual mill speed in rpm (percent of criticla speed)
  11 .Water weight and mass: 	62.42 lbs/〖ft〗^3 = 1.9385 slugs/〖ft〗^3 
  12. Volume: 1 m^3  = 1000 〖dm〗^3 liters= 35.288 〖ft〗^3  = 1.305 〖yd〗^3
  13. Weight/Mass of water 1 g/〖cm〗^3 = 1  g/ml (4 deg C at sea level)
  								  = 1 kg/liter 
                                    = 1000 kg/m^3 = 1 tonnes/m^3 
                                    = 62.4 lbs/〖ft〗^3 
                                    = 8.34 (lbs)/gal
  14. Conversion for water volume: 	7.473(lbs)/gal ≈ 1 lbs/〖ft〗^3   
  15. Refined iron ore weight:		≈449.42 lbs/〖ft〗^3
  16. Crushed iron ore weight	≈156.07 lbs/〖ft〗^3
  17. SAG mill overflow		SG=2.6 (needs to be confirmed mathematically--direct measurement takes drying time)
  18. Kilowatts per ton for rod mill:   	kwr=〖1.07〗^0.34 (6.3-5.4∙Vp)∙%Cs kw/ton=kw/Tr
  19. Power draw:  			Prm=Tr∙kwr 
  20. Critical Speed formula (rod mill):	
  				D(Csr)^2=76.63 (constant for a rod mill needs adjustment for a SAG mill)  
  				Cs=76.63/√D (critical speed isolated)
  21. When ρ of ref=ρ of water (@ 4°C): 	S.G.=ρ_material = ρ of material/ρ of water = ρ_material/1.00 
  22. Linear conversion factor		1m ≈ 3.28 ft

###Images
####This is a picture of the grinding material in a SAG mill. One of the programs calculates the volume of this material

![SAG Mill Grinding Material](https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcQfh6zXYG7pJECsth2DVx44SImR4RPQfwTYwUqaSniz3nDAq6Xssw)

####This is a picture of the outside of a SAG mill. The other program calculates the circulating load of the slurry flowing through this mill.


![SAG Mill](http://photos.newswire.ca/images/download/20140206_C7934_PHOTO_EN_36350.jpg)

####This is one of the pieces of equipment that kept breaking down from not having a good management tool

![Flowtation Tank](http://cadillapp.com/assets/templates/1410898792/b34d27579fac962dd7ab8083f8e61f031376c555.jpg)



