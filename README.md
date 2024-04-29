# systemDesign

graph TD
    Start((Start))
    Start --> DefineRequirements((Define Requirements))
    DefineRequirements --> DesignHighLevel((Design High-Level Architecture))
    DesignHighLevel --> DecomposeSubmodules((Decompose into Sub-modules))
    DecomposeSubmodules --> RefineSubmoduleFunctionality((Refine Sub-module Functionality))
    RefineSubmoduleFunctionality -->|If Sub-module complex| DecomposeFurther((Decompose further into Sub-modules))
    RefineSubmoduleFunctionality -->|End of Sub-module refinement| RefineInterfaces((Refine Interfaces))
    DecomposeFurther --> RefineSubmoduleFunctionality
    RefineInterfaces --> CodeModules((Code Modules))
    CodeModules --> IntegrateModules((Integrate Modules))
    IntegrateModules --> TestDebug((Test & Debug))
    TestDebug --> SystemComplete((System Complete?))
    SystemComplete -->|No| GoBack((Go back to Integration Step))
    SystemComplete -->|Yes| End((End))
    GoBack --> IntegrateModules
