Collab link: https://colab.research.google.com/drive/1svazfEQdtZpc112gNrDvZjj17PdvLC8H?usp=sharing#scrollTo=pklSMqmRp1Gh
**Dynamic Pricing for Urban Parking Lots: **

_**Models Implemented: **_

 

_Model 1:  _

Simple rule-based adjustment: 
_
Price (at t+1) = Price (at t) + alpha*(occupancy/Capacity) _

Base Price: $10 

Price Range: Clamped between $5 and $20 

Acts as a reference model to observe how occupancy directly influences pricing 

_Model 2: _

A more intelligent pricing model using a custom demand function: 

_Demand= alpha*OccupancyRate+b*QueueLength-c*Traffic+d*SpecialDay +e*VehicleTypeWeight _

VehicleTypeWeight: Car=1.0, Bike=0.5, Truck=1.5 

Pricing Formula: 

_Price =BasePrice*(1+lambda*NormalizedDemand) _

This model allows for dynamic adjustments based on multiple real-world variables. 

Constraints: Prices are bounded to avoid erratic spikes or drops. 

 

 

Data is streamed using Pathway, mimicking real-time updates. 

Models are hooked into the pipeline to emit continuous price predictions. 

Enables real-time pricing decisions for each time interval and lot 
