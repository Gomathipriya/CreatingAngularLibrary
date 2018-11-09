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

7. Create 
