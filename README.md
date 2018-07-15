# Java_EE_Udemy20
Stateful Session Enterprise Java Beans
#This tutorial highlighted the issue of creating a stateless and stateful session Enterprise Java Bean
If both are using the same EJB a conflict will appear.
This is because Eclipse and Glassfish do not know which EJB to use
The remedy is to name each EJB
in this case @Stateless(name = "flightStateless") and @Stateful(name = "flightStateful") 
can then be used as:
  @EJB(beanName = "flightStateless")
	private FlightLocal_ejb8 fs;
	
	@EJB(beanName = "flightStateful")
	private FlightLocal_ejb8 fsStateful;
