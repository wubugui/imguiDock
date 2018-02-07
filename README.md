## imguiDock

An addon of [imgui](https://github.com/ocornut/imgui/wiki) for support dock in the window

这是一个[imgui](https://github.com/ocornut/imgui/wiki)的dock插件。

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/134486032@N03/24660622177/in/dateposted-public/" title="QQ图片20180106100302"><img src="https://farm5.staticflickr.com/4683/24660622177_7dafeee6e1_c.jpg" width="800" height="621" alt="QQ图片20180106100302"></a>

## How to use（使用指南）
```cpp
void setup(){
	// auto-load the imgui.ini settings
	//自动加载imgui.ini设置
	ImGui::InitDock();
}

void update(){
	if(ImGui::Begin("Dock Demo"))
	{
		// dock layout by hard-coded or .ini file
		// 硬编码或者从ini文件确定dock布局.
		ImGui::BeginDockspace();

		if(ImGui::BeginDock("Dock 1")){
			ImGui::Text("Hi");
		}
		ImGui::EndDock();

		if(ImGui::BeginDock("Dock 2")){
			ImGui::Text("I'm BentleyBlanks!");
		}
		ImGui::EndDock();

		if(ImGui::BeginDock("Dock 3")){
			ImGui::Text("Hello World");
		}
		ImGui::EndDock();

		ImGui::EndDockspace();
	}
	ImGui::End();
	
	// multiple dockspace supported
	// 支持多dockspace
	if(ImGui::Begin("Dock Demo2"))
	{
		ImGui::BeginDockspace();

		if(ImGui::BeginDock("Dock 1")){
			ImGui::Text("Hi");
		}
		ImGui::EndDock();

		if(ImGui::BeginDock("Dock 2")){
			ImGui::Text("I'm BentleyBlanks!");
		}
		ImGui::EndDock();

		if(ImGui::BeginDock("Dock 3")){
			ImGui::Text("Hello World");
		}
		ImGui::EndDock();

		ImGui::EndDockspace();
	}
	ImGui::End();
}

```

## Intro（介绍）

Thx to the [nem0](https://github.com/nem0), [paniq](https://github.com/paniq), [adcox](https://github.com/adcox)'s distribute of ```imgui_dock```, so the imgui_dock was able to ```auto save/load``` to/from the ```imgui.ini```.

> It seems the [Lumix Engine](https://github.com/nem0/LumixEngine) have done a quite intelligible work just save the dock's property to a Lua file, so I was just save the properties to the ```imgui.ini```.(you can modify the format if you want)

> Some complie errors may occured because of the API change of ImGui, pls let me know

## Collaborator（贡献者）
1. [LonelyWaiting](https://github.com/lonelyWaiting)
2. [BentleyBlanks](https://github.com/BentleyBlanks)
3. [Wubugui](https://github.com/wubugui)
