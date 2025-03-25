# Report:

The IAM4NFDI team has set up a new WissKI tenant in didmos that users can log into with the NFDI-AAI infrastructure and currently supports login via DFN-AAI.
The tenant also allows the SODa team to manage groups and permissions on a user-level basis that can be passed down into the individual services, to provide a group and role assignment.
The SODa team has set up a central Keycloak instance in the context of the SCS to provide a centralized login solution for the hosted WissKI systems.
It is connected to the previously mentioned WissKI tenant of the the centrally hosted multi-tenant didmos instance, which serves as a proxy for the login via DFN-AAI or edu-id proxy in the future, once it is available.
The Keycloak instance serves as an intermediate the proxy between the various WissKI systems and didmos.
The solution with this intermediary Keycloak was chosen because it allows automatic registration of new systems via a REST API, and thus eliminates the otherwise manual registration process that comes with integrating new systems into the NFDI-AAI infrastructure.
Another benefit of this setup is that the SCS can also use this Keycloak to integrate other SSO-capable SCS services, like e.g. JupyterHub to the NFDI-AAI infastructure to provide a seamless user-experience within the SCS.

