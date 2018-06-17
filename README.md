# UNDER CONSTRUCTION

# ASP.NET-Web-Project-Starter
Basic clean architecture for an asp.net web project

3 layers - 
1. Web/UI/Presentation Layer
2. Domain/Core/Business Layer (The Abstraction Layer)
3. Data/Infrastructure Layer

- Layers 1 and 3 should point to layer 2 at the core

- UI layer should use DI - in an ideal world we would not have an explicit reference to data layer in our UI layer. But, as we will only reference it in the global.asax/startup.cs (in other words or 'composition root') and not any other UI related project files then it technically is okay. However, I still dont fully like the idea of having it there. One possible solution is to use StructureMap as shown [here](https://github.com/CleanDDD/NoInfrastructureReferences/tree/master/mvc5/CleanGuestbookMvc5). Original article [here](https://ardalis.com/avoid-referencing-infrastructure-in-visual-studio-solutions)

- Abstractions should not depend upon details. Details should depend upon abstractions = domain-layer should have no dependencies

- combine repo and specification patterns for data access layer
