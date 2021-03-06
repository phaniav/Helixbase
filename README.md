<img src="https://nshackblog.files.wordpress.com/2017/02/helixbase1.png" height="154px" width="200px" /><br />
A Sitecore Helix based solution which can be used for Greenfield projects. Tackles some common problems when working with the platform.

#### Features include:

* Glass Mapper (using fluent configuration)
* Unicorn - including user and role sync
* Sitecore 8.2 Update-2 ready
* Bootstrap
* Target .net framework 4.5.2 for backwards compatibility
* Sitecore Dependency Injection - with auto controller registration
* A sample hero banner feature and sample site project for demonstration
* Generic item repositories - includes content API and search API
* 301 Redirects
* Version trimming rules engine - Items limited to 10 versions

#### Coming soon:

* Multisite datasource
* Non admin file unlock

## Setup Instructions
1. Install <a href="https://dev.sitecore.net/Downloads/Sitecore_Experience_Platform/82/Sitecore_Experience_Platform_82_Update2.aspx" target="_blank">Sitecore Experience Platform 8.2 rev. 161221 (8.2 Update-2)</a>
	1. _Name your instance 'demo.helixbase'_
2. Clone project to 'C:\Projects\Helix base'
	2. _If you use another path, update the 'z.Helixbase.Settings.config' file and the 'gulp-config.js'_
3. Install <a href="https://nodejs.org/en/" target="_blank">Node.js</a> and run 'npm-install' in the project root
4. Perform a Nuget restore
5. Publish each project in VS, or view gulp tasks - you may need to update the 'MSBuildToolsVersion' in the gulp-config.js
6. Run Unicorn and sync all configurations

#### Using Helix Base:
Refer to the <a href="https://github.com/muso31/Helixbase/tree/master/src/Feature/Hero/code">Hero Feature</a> as an example.

* View <a href="https://github.com/muso31/Helixbase/blob/master/src/Feature/Hero/code/Service/HeroService.cs">HeroService.cs</a> for examples of how to get an item from Sitecore using the content API and the search API.
* View <a href="https://github.com/muso31/Helixbase/blob/master/src/Feature/Hero/code/Routes/RegisterRoutes.cs">Register routes</a> for an example of how to register a route.

To add a 301 redirect simply add a redirect item to the _Redirect Items_ folder found in your site _Global_ folder.

To change the item version limit edit the rule on the _/sitecore/system/Settings/Rules/Item Saved/Rules/Delete Old Versions_ item. You can also change the rule to recycle or archive old versions. 