## Angular Material Docs Site   
A repository storing the `dist` output from [Angular's Components repo](https://github.com/angular/components), located within the [`material.angular.io` folder](https://github.com/angular/components/tree/main/material.angular.io).

## To update
1. Clone down this repo 
1. Clone down the Angular Componets repo https://github.com/angular/components.git in another location
1. `cd` into `material.angular.io` folder
1. Run `yarn install` 
   - you may need to globally install `yarn` via `npm install -g yarn` first
1. Edit the `angular.json` `outputHashing` to be set to `none` (there's 2 of them)  
1. Run `yarn build:content`
   - This command doesn't always work it seems. It's in their original README so we include it just in case. If it fails, proceed to next step
1. Run `yarn start` to verify site works
1. If site works, run `yarn prod-build` to build out the `dist`
1. Once script finishes, run `serve dist` to verify build works (kill process once complete)
   - You may need to globally install `serve` via `npm install -g serve` first
1. Copy the contents of `dist/material-angular-io` into this repo's `material-angular-io`
1. Verify the site still works by running `npm run start` to re-verify the build works
1. Commit & push changes
