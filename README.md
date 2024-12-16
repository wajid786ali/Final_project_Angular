# WajidP

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 18.0.6.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.


1. Employe - done
   - Employe Register
   - Employe List
   - Employe Update
2. Company - panding
   - Company Register
   - Company List
   - Company Update


================================
added: json-server --watch db.json
Add JSON server to package.json scripts:
"scripts": { "start:json": "json-server --watch db.json --port 3000"}
npm run start:json
================================
Steps to Merge ng serve and npm run start:json:
Install concurrently:
Copy code-----
npm install concurrently --save-dev
Update package.json: Add a new script in the scripts section:

Copy code------
"scripts": {
  "start": "concurrently \"ng serve\" \"npm run start:json\"",
  "start:json": "json-server --watch db.json --port 3000"
}
Run Both Servers: Use the single command:
npm start
================================
