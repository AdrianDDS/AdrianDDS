# SABER ANIMATION/RIGGING TOOLS TEST

This is a project developed for the test that proposes Saber.

The test consists of developing a tool for Maya & Max using Python 2 and their respectives scripting languages.

## Installation & Usage

In order for this demo to work both in maya & max is mandatory to change the variable my_path in the file main.py inside the scripts folder to match the path in where this folder was unzip.

Example: 


```python
my_path = "C:\\Path\\where\\unzip\\this\\EntregaSaber\\Scripts"
```

Once this is changed, one only needs to run the said script main.py in Max or Maya (examples of how to do it can be found in both videos in the Docs folder)


## Folder Structure:

EntregaSaber/
|	Scripts/
|		├── Interface/
|		|  ├─ __init__
|		|  └─ ToolMenu
|		|
|		├── Managers/
|		|  ├─ __init__
|		|  ├─ MngBasic
|		|  ├─ MngMax 
|		|  └─ MngMaya 
|		|
|		├─ __init__
|		└─ main	
|
|	Docs/
|		├─ SaberDemoMax
|		└─ SaberDemoMaya
|
└─ README

### main.py

The script needed to run from Maya or Max in order to use the tool. As mentioned in Installation & Usage, is necessary to adjust the variable my_path. Once this is donde the script can be run in both softwares.

Its main functionality consists in detecting if it's running over Max or Maya and load the necessary Manager classes and the Menu UI.

### Interface

Contains the basic clase for the Menu UI : ToolMenu. This can be expanded or complemented with other clases to add functionality.

### Managers

This package contains the base class for crating managers for the API's : MngBasic. In this example, this class is expanded by the derived classes MngMax & MngMaya. Depending of the initialization in main.py only one of this clases will be used to perform the operations over the corresponding objects in the desired app.

### Docs

This folder contains two videos showing the tool in both Max & Maya.