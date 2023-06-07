# MDK-DemoSampleApp
exercise to develop a MDK project on BAS and VC

## On VC
Prerequisites
following the tutorials below
https://developers.sap.com/tutorials/cp-mobile-dev-kit-build-client.html

### Deploying to Mobile Services
https://help.sap.com/doc/f53c64b93e5140918d676b927a3cd65b/Cloud/en-US/docs-en/guides/getting-started/mdk/vscode/deploying-to-mobile-services.html

1. Editar .vscode/settings.json
    - "mdk.mobileservice": {
        "adminAPI": "https://mobile-service-cockpit-web.cfapps.us10.hana.ondemand.com/cockpit/v1/org/d42dc380trial/space/dev",
        "appId": "com.sap.mdk.demo"
      }
2. Right click on Application.app and press MDK: deploy
3. Usar en el login, el usuario del Mobile Services, en este caso leonelwillian.moralescanahualpa@nttdata.com
4. If the error bellow appears, follow [https://answers.sap.com/questions/13873745/error-deploying-mdk-application-in-mobile-services.html]
App update failed, will roll back to previous metadata definitions Reason: Invalid call to DefinitionProvider.getApplicationDefinition sPath is undefined

### Deploying to local mdkclient

1. Edit .vscode/settings.json
    - "mdk.debugAppRoot": "C:\\Users\\lmoralca\\Documents\\trials\\MDK\\DemoAndMdkclient\\MDKClient-DemoSampleApp\\DemoSampleApp"
    - "mdk.autoBundle": true
    - "mdk.targetClient": "MDK 6.x"
2. On Command Palette
    - Tasks: Run Bundle Task
    - MDK bundle build
3. On DemoSampleApp generated directory
    - tns run android --device 18ABCDEFGH
    or
    - tns run android --emulate