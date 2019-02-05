# Getting-Started-With-Unreal-Engine4-And-Paper2d
This is a guide specific to setting up Paper2D with a C++ Unreal Engine 4 Project. There isn't alot of information on this out there without scowering the internet or AnswersHub. So I took it upon myself to create a guide for newcomers to hopefully remove some early frustrations whilst creating your new Paper2D project.

# Step One
 If for some reason, you don't already have Unreal Engine installed. Install Unreal Engine 4 via:
 https://docs.unrealengine.com/en-US/GettingStarted/Installation
 
# Step Two
 Launch UE4 with the EPic Launcher and create a new Basic Code C++ Project. 
 
# Step Three
 If the Editor hasn't launched it already, Click file in your editor, and in the drop down select "Open Visual Studio".
 
# Step Four
With Visual Studio open, locate "YourProjectName.Build.cs" in the Solution Explorer and open that file.

# Step Five
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


                                               
