BEFORE WE BEGIN, REMEMBER

- Keep the mod naming to values like: ExampleMod, TimeDateMod, etc. following Class name conventions.  https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-classes-structs-and-interfaces

- Keep the namespace to values like: Creator.Example, Jixxed.TimeDate, etc. following namespace conventions.  https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-namespaces


Creating a unity mod

This guide will help you build your first mod and load it in the game. You can adapt it afterwards to your needs. This guide is written Unity version 2021.2.13f1. (update?)

Additionally, this guide assumes you have already followed the instructions the Stationeers-mods guide located here -> link

It also assumes you have installed the following software specified in the guide found here -> link


Unity 2022.3.7f1 - link
Unity Explorer - link - instructions link
dnSpy - link - instructions link



Import Template
	- Download the ExampleMod. This contains a working starter mod you can easily adapt.
	- Make sure you have followed the instructions included in the Git Hub to properly have this environment ready to go. Skipping this will invalidate the instructions provided here.
		- Copy the project into a project folder (ex. ExampleMod)
	- Update the StationeersMods exporter plugin for Unity with the latest version of StationeerMods-exporter.zip - https://github.com/jixxed/StationeersMods/releases/download/v1.0.30.0/StationeersMods-exporter.zip
		•  Overwrite files in the location with those downloaded.


Prerequisites and Assemblies

 - Open the Unity Editor
 - In the Unity Editor, look to the project window which by default is in the bottom of the screen

![image](https://github.com/user-attachments/assets/7affb80f-5cc4-4c0c-a58e-12306162ab0d)


- Go to **Assets > Assemblies** and open the .txt file named **Copy.txt**

![image](https://github.com/user-attachments/assets/0c57a13c-9199-40e8-bf77-b1c22978826e)


- This lists all the assemblies you need (dll's)
