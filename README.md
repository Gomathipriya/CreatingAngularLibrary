# CreatingAngularLibrary
How to create angular library using ng-packagr

1. Create a new Project using 

<code> ng new projectname </code>

2. Create a new module using 

<code> ng g module moduleName </code>

3. Create new component by navigating to the module "cd src/app/moduleName"

<code> ng g component componentName </code>

4. Export the component in the module

5. Install ng-packagr using <code> npm install ng-packagr </code>
  
6. Create public_api.ts file. Export all the modules and components to be used as library

<pre> Example  
    export { moduleName } from './src/app/moduleName.module';
    export { componentName } from './src/app/componentName.component';
</pre>

7. Create ng-package.json like below
<pre>
{
  "$schema": "./node_modules/ng-packagr/ng-package.schema.json",
  "lib": {
    "entryFile": "public_api.ts"
  }
}
</pre>

8. Remove target and module from tsconfig.json file and   change "typescript": "2.9.2" in package.json

9. In package.json make private as true, update the version and add the below script 

<code> "packagr": "ng-packagr -p ng-package.json" </code>

10. Remove ng-packagr from dependencies and change dependencies to "peerDependencies".

11. Now run <code> npm run packagr </code>

12. You can see the code is packaged in dist folder.

13. Change directory to dist and run <code> npm pack </code>

14. We can get a tar file.


<pre>
Note: Have all the HTML code and CSS code inside typescript
</pre>


