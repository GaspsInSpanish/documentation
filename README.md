# **Modding Stationeers In Unity**

BEFORE WE BEGIN, REMEMBER

- Keep the mod naming to values like: ExampleMod, TimeDateMod, etc. following Class name conventions.  https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-classes-structs-and-interfaces

- Keep the namespace to values like: Creator.Example, Jixxed.TimeDate, etc. following namespace conventions.  https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-namespaces


## **Creating a unity mod**

This guide will help you build your first mod and load it in the game. You can adapt it afterwards to your needs. This guide is written Unity version 2021.2.13f1. (update?)

Additionally, this guide assumes you have already followed the instructions the Stationeers-mods guide located here -> link

It also assumes you have installed the following software specified in the guide found here -> link


Unity 2022.3.7f1 - link
Unity Explorer - link - instructions link
dnSpy - link - instructions link


### TMP Fix
The game uses TextMeshPro. TextMeshPro is brought down after the project is opened in Unity. However, there is a bug in the TMP Code you can patch by replacing 2 files in:

<table>
OS	PATH
Windows	%localappdata%\Unity\cache\packages\packages.unity.com\com.unity.textmeshpro@3.0.6\Scripts\Runtime
Linux	~/.config/unity3d/cache/packages/packages.unity.com/com.unity.textmeshpro@3.0.6/Scripts/Runtime
</table>
You can get the files from [TMP_Fix.zip]https://github.com/jixxed/StationeersMods/blob/main/doc/TMP_Fix.zip.

This is a one time patch, since every new project will use the files from that location. Follow the steps below before proceeding so you aren't having to re-duplicate effort later.

- If you haven't already, open **Unity Hub** and then click on **New Project**
![image](https://github.com/user-attachments/assets/dbf67858-ed4a-4433-becc-e93071581616)

- Once the new project is made, and Unity Editor has opened, open the PATH to the location where the files for TextMeshPro are.
- Copy the files from the downloaded zip into the Runtime folder
- Close unity editor and delete the project
 

### Import Template
	- Download the ExampleMod. This contains a working starter mod you can easily adapt.
	- Make sure you have followed the instructions included in the Git Hub to properly have this environment ready to go. Skipping this will invalidate the instructions provided here.
		- Copy the project into a project folder (ex. ExampleMod)
	- Update the StationeersMods exporter plugin for Unity with the latest version of StationeerMods-exporter.zip - https://github.com/jixxed/StationeersMods/releases/download/v1.0.30.0/StationeersMods-exporter.zip
		•  Overwrite files in the location with those downloaded.


## Prerequisites and Assemblies

 - Open the Unity Editor
 - In the Unity Editor, look to the project window which by default is in the bottom of the screen

![image](https://github.com/user-attachments/assets/7affb80f-5cc4-4c0c-a58e-12306162ab0d)


- Go to **Assets > Assemblies** and open the .txt file named **Copy.txt**

![image](https://github.com/user-attachments/assets/0c57a13c-9199-40e8-bf77-b1c22978826e)


- This lists all the assemblies you need (dll's)
- You will likely get a failure to compile and a window like the one below. These are usually related to assemblies failing and may be resolved manually. Make sure to read the error carefully and look back through documentation. 
![image](https://github.com/user-attachments/assets/b98fb883-06cc-4115-ab3b-630c1abc3f8f)

- Once you are in the project you should see the following or something similar along the top menu bar.
![image](https://github.com/user-attachments/assets/6cefd6a9-2fae-42b7-9354-67b455f980ad)

- Click **StaitoneersMods** and then **Export Settings**

![image](https://github.com/user-attachments/assets/2290a45d-2952-48bf-a934-e8e4358792b4)

- Move the new window down to your lower Panel where **Project** and **Console** should already be by default (you can do this by dragging the tab down the same way you can drag tabs on a web browser.
![image](https://github.com/user-attachments/assets/d45bfd2e-2154-4930-b83b-daa43d172e68)


### **Copy assemblies**
To copy the assemblies you can click the button in the editor. Make sure you have the Stationeers game folder set in the exporter settings. This action will copy over all the assemblies defined in the copy.txt file. Be aware that the game might add new assemblies in the future, so you might need to update this list.

![image](https://github.com/user-attachments/assets/d2e2dc90-20d1-4d9a-a1de-d765304b6650)

### Unity Editor
Once the project is imported you can check the asmdef in the Scripts folder. it should look like this:

![image](https://github.com/user-attachments/assets/2dcdd15a-67ef-41e8-adb7-e115360fdcf0)


(Work)

## **Building The Project**

To build the mod you can open the exporter from the menu

![image](https://github.com/user-attachments/assets/217e65d4-2827-42fe-afab-bc6bd450fa4a)

Fill in the settings:

* Mod name: Name of your mod
* Author: Your (nick)name
* Version: Version of the mod
* Description: Description for your mod
* Include Content: Content to include. For this example it will be Everything
* Startup Type: Type of startup class. For this example it will be Code
* Startup class: Name of the startup class
* Output Directory: Description for your mod (set this to your local mods folder)
