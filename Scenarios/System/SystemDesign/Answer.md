I always consider Simon Sineks Goldern circle when embarking on delivering solutions to problems. Although the context in which he discusses the principles is in business strategy I believe that it is applicable and important in solution desing. Here is a short video of him explaining https://youtu.be/Jeg3lIK8lro.

![Simon Senik - The Goldern circle](image.png) The goldern circle - Simon Sinek

The WHY is defined in the scenario - to monitor the health of large machinery at their fascilities.

The WHAT is also briefly explained in the scenario - "Management wants you to create a web application service". However, the underlying solution (the web application) is yet to be discovered. Hence my approach would be to firstly focus on the essence of WHAT this this application is solving.

The HOW will be uncovered by the majority of this document - How would you go about designing and implementing the system?

=========================================================================================================================

The choice of the approach is motivated by the nature of the requirement. The requirement is quite general and the ideal solution needs to be uncovered in a series of iterations for the solution to derive value in a timely and cost effective manner. The design and implementation approach of such an application would include gathering requirements, planning, analysis, designing, building, testing, deployment and evaluating phases.

### Planning and requirements analysis:

Initially, determing the stakeholders' and/or clients' needs, and systems requirements is important to establish by engaging with the potential clients to better understand their requirements for machinery monitoring in the web application. This is expected to cover information regarding the types of machines, data that needs to be tracked, the frequency at which data needs to be updated, any specific details in the form of notifications or reporting, and so on. The solution will have a special focus on integration with existing services, scalability, security, and customer satisfaction. 

Once the requirements have been gathered (The WHAT), a scope of the system needs to be drawn in order for the project timelines to be established and avoid building features that are out of scope. The scope will be broken down into manageable iterations and planned according to the project timeline using an iterative project management method. 

After the above has been discovered, an analysis of the requirements needs to be done where the WHAT is modeled then after, the focus would shift to HOW the solution will be designed and implemented. Below is an outline of the approach.

### Method
The method used to design and implement the solution will be an iterative process where the goal is reached in a series of ever improving delivery cycles as depicted in the image below. The implementation is a series of short mini projects. Each iteration gives a tested, integrated and executable system.

![Iterative process](image-1.png) Iterative process

This method is greatly for this kind of task where the risk of the project failing is greatly reduced by taking one shot at the project and steering the way to success using information instead of launching blindly to the unknown. High priority features aree developed first and user feedback is gathered and the cycle repeats until the requirements are met.

### Design

---TODO
---In addition to uncovering what needs to be done, the service model needs to be defined, including the price per license. Determining the definition for a "license" in the context of the service provided is crucial (for example, is the application licensed per volume of data handled, per machine registered etc.).


---I would implement an agile development methodology in the way of a lifecycle of the the project that ensures iterative development, sustainable feedback and adaptation to changing needs. See development approach below:

Architecture: Before initiating the development of any solution, it is crucial to establish a design of the architecture of the application to support the manifestation of the idea. To support the growth of the system and at the same time flexibility, I would adopt a microservice-architecture considering that the application would integrate with existing and future services. A mircoservices will allow independent development, deployment, and scalable services for the application. The modularity of the architecture will enable future services to be developed and extended within the system.

Databases: The scenario has already outlined the databses that are being used. For large transactional/ unstructured data, a non-relational database like Mongodb will be applicable to scalability and flexibility as suggested. On the other hand, for masterdata and service configuration data, a relational database like MySQL will be considered. 
 
API integration: Develop RESTful APIs that are connected with existing and future services, allowing retrieval of monitoring data; ensuring that these APIs are secure, scalable, and well documented. Security of the application should be ensured by adequate authentication and authorization mechanisms like OAuth2 and JWT, data encryption for sensitive data and periodic security audits. 

### Implementation / Development

Frontend: Develop user interfaces that the user interacts with to configure service, view machine health metrics and get notifications. To achieve this, I would adopt the use of morden, responsive, and interactive UIs using either front-end development frameworks such as Angular, Vuejs or React for modularity and scalability. 

Backend: Implement the earlier designed Restful APIs such that they expose functionality of the system securely. Moreover, ensure that the system is well integrated with the services required in place by the use of APIs in data exchanfe and extending functionality.

