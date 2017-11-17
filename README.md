INSTRUCTIONS

Download solution

Download the Nuget packages

Build solution

Execute the Utiltiy Project

Execute the Unit Tests project

Execute the Web Project, navigate to the PetsTest.html page to run the JavaScript unit tests

SOLUTION DESCRIPTION

The solution consists of 5 projects.

AGL.Pets.Common contains interfaces used for dependency injection (Castle).

AGL.Pets.Domain contains two classes (Person, Pet) used to deserialize the Json data etc.

AGL.Pets.UnitTests contains tests for the PersonsRepository.GetPets...

AGL.Pets.Utiltity is a Windows Console app project. This project defines a PersonRepository class which is used to list Pets in the requested structure described by the coding challenge.

A web project to demonstrate a testable JavaScript version

The Utiltity project also defines a DataContext class that is used by the repository to retrieve data. This DataContext class is an implementation of an IDataContext class which is injected (using Property Injection and the Castle Window IoC framework). The concrete implementations of IDataContext includes a version which does not download Json data from the API service called FakeDataContext. This is useful for debugging, so the WindowsInstaller defines this as the concrete class for IDataContext given a pre-compiler directive of DEBUG.

Three Unit Tests target the PersonReporitoy method GetCatsByOwnerGender. The tests cover three cases:

Valid data and successful execution

Border case valid data and successful execution

Invalid data with an expected exception

NOTE

Further improvements would include

Custom exception handling.

Extracting the DataContext and Repositories to a seperate project# AGL
