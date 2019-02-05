# WIP

# Getting-Started-With-Unreal-Engine4-And-Paper2d
This is a guide specific to setting up Paper2D with a C++ Unreal Engine 4 Project. I created this guide for newcomers to hopefully remove some early frustrations while creating your new Paper2D project.

# Step One: Installation
 If for some reason, you don't already have Unreal Engine installed. Install Unreal Engine 4 via:
 https://docs.unrealengine.com/en-US/GettingStarted/Installation
 
# Step Two: Create New Project
 Launch UE4 with the EPic Launcher and create a new Basic Code C++ Project. 
 
# Step Three: Open Visual Studio
 If the Editor hasn't launched it already, Click file in your editor, and in the drop down select "Open Visual Studio".
 
# Step Four: Open Build.cs 
With Visual Studio open, locate "YourProjectName.Build.cs" in the Solution Explorer and open that file.

# Step Five: Add Paper2D Dependency to Build.cs file & Project
Add "Paper2D" to the PublicDependencyModuleNames.AddRange(... {...}); list of dependencies.

```c#
// Fill out your copyright notice in the Description page of Project Settings.

using UnrealBuildTool;

public class YourProjectName : ModuleRules
{
	public YourProjectName(ReadOnlyTargetRules Target) : base(Target)
	{
		PCHUsage = PCHUsageMode.UseExplicitOrSharedPCHs;
	
		PublicDependencyModuleNames.AddRange(new string[] { "Core", "CoreUObject", "Engine", "InputCore", "Paper2D" });
		PrivateDependencyModuleNames.AddRange(new string[] {  });

		// Uncomment if you are using Slate UI
		// PrivateDependencyModuleNames.AddRange(new string[] { "Slate", "SlateCore" });
		
		// Uncomment if you are using online features
		// PrivateDependencyModuleNames.Add("OnlineSubsystem");

		// To include OnlineSubsystemSteam, add it to the plugins section in your uproject file with the Enabled attribute set to true
	}
}
```

# Step Six: Refresh Visual Studio From UE4 Editor
With the UE4 Editor open select the "File Drop Down" and select "Refresh Visual Studio"

# Step 7: Enjoy!

## Success! All Paper2d headers and classes should be working properly and recognized by Intellisense!

                                               
