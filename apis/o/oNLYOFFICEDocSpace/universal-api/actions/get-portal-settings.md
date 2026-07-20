# ONLYOFFICE DocSpace: Get Portal Settings

Retrieves portal settings from ONLYOFFICE DocSpace.

```
GET https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ONLYOFFICE DocSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-portal-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "baseDomain": "string",
      "cookieSettingsEnabled": true,
      "culture": "string",
      "debugInfo": true,
      "deepLink": {
        "androidPackageName": "https://example.com",
        "iosPackageId": "https://example.com",
        "url": "https://example.com"
      },
      "displayAbout": true,
      "displayBanners": true,
      "docSpace": true,
      "domainValidator": {
        "maxLength": 1,
        "minLength": 1,
        "regex": "string"
      },
      "enableAdmMess": true,
      "externalResources": {
        "api": {
          "domain": "string",
          "entries": {
            "docspace": "string",
            "javascriptSdk": "string",
            "pluginsSdk": "string"
          }
        },
        "common": {
          "entries": {
            "booktrainingemail": "ava@example.com",
            "documentationemail": "ava@example.com",
            "feedback": "string",
            "legalterms": "string",
            "license": "string",
            "paymentemail": "ava@example.com",
            "supportemail": "ava@example.com"
          }
        },
        "forum": {
          "domain": "string"
        },
        "helpcenter": {
          "domain": "string",
          "entries": {
            "accessrights": "string",
            "administrationguides": "string",
            "administratormessage": "string",
            "aisettings": "string",
            "alternativeurl": "https://example.com",
            "apikeys": "string",
            "appearance": "string",
            "autobackup": "string",
            "becometranslator": "string",
            "configureDeepLink": "https://example.com",
            "configuringsettings": "string",
            "connectamazon": "string",
            "connectapple": "string",
            "connectbox": "string",
            "connectdropbox": "string",
            "connectfacebook": "string",
            "connectfirebase": "string",
            "connectgoogle": "string",
            "connectgooglecloudstorage": "string",
            "connectlinkedin": "https://example.com",
            "connectmicrosoft": "string",
            "connectonedrive": "string",
            "connectrackspace": "string",
            "connecttelegram": "string",
            "connecttwitter": "string",
            "connectwechat": "string",
            "connectzoom": "string",
            "creatingbackup": "string",
            "dataImport": "string",
            "docspacefaq": "string",
            "docspacemanagingrooms": "string",
            "documentService": "string",
            "encryption": "string",
            "enterpriseinstall": "string",
            "enterpriseinstallscript": "string",
            "enterpriseinstallwindows": "string",
            "integrationsettings": "string",
            "invitationSettings": "string",
            "ipsecurity": "string",
            "language": "string",
            "ldap": "string",
            "limiteddevtools": "string",
            "login": "string",
            "managingusers": "string",
            "oauth": "string",
            "passwordstrength": "string",
            "pluginsSdk": "string",
            "renaming": "string",
            "sessionlifetime": "string",
            "settings": "string",
            "singleSignOn": "string",
            "smtp": "string",
            "storagemanagement": "string",
            "trusteddomain": "string",
            "twofactorauthentication": "string",
            "userguides": "string",
            "welcomepage": "string"
          }
        },
        "integrations": {
          "entries": {
            "drupal": "string",
            "pipedrive": "string",
            "wordpress": "string",
            "zapier": "string",
            "zoom": "string"
          }
        },
        "site": {
          "domain": "string",
          "entries": {
            "allconnectors": "string",
            "buydeveloper": "string",
            "buyenterprise": "string",
            "collaborationrooms": "string",
            "customrooms": "string",
            "demoorder": "string",
            "desktop": "string",
            "docspace": "string",
            "docspaceprices": "string",
            "downloaddesktop": "string",
            "downloadmobile": "string",
            "forenterprises": "string",
            "formfillingrooms": "string",
            "officeforandroid": "string",
            "officefordrupal": "string",
            "officeforios": "string",
            "officeforwordpress": "string",
            "officeforzapier": "string",
            "officeforzoom": "string",
            "openai": "string",
            "privaterooms": "string",
            "publicrooms": "string",
            "registrationcanceled": "string",
            "seamlesscollaboration": "string",
            "subscribe": "string",
            "wrongportalname": "Ava Chen"
          }
        },
        "socialNetworks": {
          "entries": {
            "facebook": "string",
            "instagram": "string",
            "tiktok": "string",
            "twitter": "string",
            "youtube": "string"
          }
        },
        "support": {
          "domain": "string",
          "entries": {
            "request": "string"
          }
        },
        "videoguides": {
          "domain": "string",
          "entries": {
            "activesessions": "string",
            "archive": "string",
            "backup": "string",
            "createfiles": "string",
            "fileversions": "string",
            "filterfiles": "string",
            "full": "string",
            "hotkeys": "string",
            "operationswithfiles": "string",
            "playlist": "string",
            "profile": "string",
            "roles": "string",
            "rooms": "string",
            "security": "string",
            "whatis": "string"
          }
        }
      },
      "firebase": {
        "apiKey": "string",
        "appId": "string",
        "authDomain": "string",
        "databaseURL": "https://example.com",
        "measurementId": "string",
        "messagingSenderId": "string",
        "projectId": "string",
        "storageBucket": "string"
      },
      "formGallery": {
        "domain": "string",
        "ext": "string",
        "path": "string",
        "uploadDashboard": "string",
        "uploadDomain": "string",
        "uploadExt": "string",
        "uploadPath": "string"
      },
      "greetingSettings": "string",
      "invitationLimit": 1,
      "isAmi": true,
      "limitedAccessDevToolsForUsers": true,
      "limitedAccessSpace": true,
      "logoText": "string",
      "maxImageUploadSize": 1,
      "nameSchemaId": "Ava Chen",
      "ownerId": "string",
      "plugins": {
        "delete": true,
        "enabled": true,
        "upload": true
      },
      "recaptchaType": 1,
      "socketUrl": "https://example.com",
      "standalone": true,
      "tagManagerId": "string",
      "tenantAlias": "string",
      "tenantStatus": 1,
      "timezone": "string",
      "trustedDomainsType": 1,
      "userNameRegex": "Ava Chen",
      "utcHoursOffset": 1,
      "utcOffset": "string",
      "version": "string",
      "zendeskKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseDomain` | string |  |
| `cookieSettingsEnabled` | boolean |  |
| `culture` | string |  |
| `debugInfo` | boolean |  |
| `deepLink.androidPackageName` | string |  |
| `deepLink.iosPackageId` | string |  |
| `deepLink.url` | string |  |
| `displayAbout` | boolean |  |
| `displayBanners` | boolean |  |
| `docSpace` | boolean |  |
| `domainValidator.maxLength` | number |  |
| `domainValidator.minLength` | number |  |
| `domainValidator.regex` | string |  |
| `enableAdmMess` | boolean |  |
| `externalResources.api.domain` | string |  |
| `externalResources.api.entries.docspace` | string |  |
| `externalResources.api.entries.javascriptSdk` | string |  |
| `externalResources.api.entries.pluginsSdk` | string |  |
| `externalResources.common.entries.booktrainingemail` | string |  |
| `externalResources.common.entries.documentationemail` | string |  |
| `externalResources.common.entries.feedback` | string |  |
| `externalResources.common.entries.legalterms` | string |  |
| `externalResources.common.entries.license` | string |  |
| `externalResources.common.entries.paymentemail` | string |  |
| `externalResources.common.entries.supportemail` | string |  |
| `externalResources.forum.domain` | string |  |
| `externalResources.helpcenter.domain` | string |  |
| `externalResources.helpcenter.entries.accessrights` | string |  |
| `externalResources.helpcenter.entries.administrationguides` | string |  |
| `externalResources.helpcenter.entries.administratormessage` | string |  |
| `externalResources.helpcenter.entries.aisettings` | string |  |
| `externalResources.helpcenter.entries.alternativeurl` | string |  |
| `externalResources.helpcenter.entries.apikeys` | string |  |
| `externalResources.helpcenter.entries.appearance` | string |  |
| `externalResources.helpcenter.entries.autobackup` | string |  |
| `externalResources.helpcenter.entries.becometranslator` | string |  |
| `externalResources.helpcenter.entries.configureDeepLink` | string |  |
| `externalResources.helpcenter.entries.configuringsettings` | string |  |
| `externalResources.helpcenter.entries.connectamazon` | string |  |
| `externalResources.helpcenter.entries.connectapple` | string |  |
| `externalResources.helpcenter.entries.connectbox` | string |  |
| `externalResources.helpcenter.entries.connectdropbox` | string |  |
| `externalResources.helpcenter.entries.connectfacebook` | string |  |
| `externalResources.helpcenter.entries.connectfirebase` | string |  |
| `externalResources.helpcenter.entries.connectgoogle` | string |  |
| `externalResources.helpcenter.entries.connectgooglecloudstorage` | string |  |
| `externalResources.helpcenter.entries.connectlinkedin` | string |  |
| `externalResources.helpcenter.entries.connectmicrosoft` | string |  |
| `externalResources.helpcenter.entries.connectonedrive` | string |  |
| `externalResources.helpcenter.entries.connectrackspace` | string |  |
| `externalResources.helpcenter.entries.connecttelegram` | string |  |
| `externalResources.helpcenter.entries.connecttwitter` | string |  |
| `externalResources.helpcenter.entries.connectwechat` | string |  |
| `externalResources.helpcenter.entries.connectzoom` | string |  |
| `externalResources.helpcenter.entries.creatingbackup` | string |  |
| `externalResources.helpcenter.entries.dataImport` | string |  |
| `externalResources.helpcenter.entries.docspacefaq` | string |  |
| `externalResources.helpcenter.entries.docspacemanagingrooms` | string |  |
| `externalResources.helpcenter.entries.documentService` | string |  |
| `externalResources.helpcenter.entries.encryption` | string |  |
| `externalResources.helpcenter.entries.enterpriseinstall` | string |  |
| `externalResources.helpcenter.entries.enterpriseinstallscript` | string |  |
| `externalResources.helpcenter.entries.enterpriseinstallwindows` | string |  |
| `externalResources.helpcenter.entries.integrationsettings` | string |  |
| `externalResources.helpcenter.entries.invitationSettings` | string |  |
| `externalResources.helpcenter.entries.ipsecurity` | string |  |
| `externalResources.helpcenter.entries.language` | string |  |
| `externalResources.helpcenter.entries.ldap` | string |  |
| `externalResources.helpcenter.entries.limiteddevtools` | string |  |
| `externalResources.helpcenter.entries.login` | string |  |
| `externalResources.helpcenter.entries.managingusers` | string |  |
| `externalResources.helpcenter.entries.oauth` | string |  |
| `externalResources.helpcenter.entries.passwordstrength` | string |  |
| `externalResources.helpcenter.entries.pluginsSdk` | string |  |
| `externalResources.helpcenter.entries.renaming` | string |  |
| `externalResources.helpcenter.entries.sessionlifetime` | string |  |
| `externalResources.helpcenter.entries.settings` | string |  |
| `externalResources.helpcenter.entries.singleSignOn` | string |  |
| `externalResources.helpcenter.entries.smtp` | string |  |
| `externalResources.helpcenter.entries.storagemanagement` | string |  |
| `externalResources.helpcenter.entries.trusteddomain` | string |  |
| `externalResources.helpcenter.entries.twofactorauthentication` | string |  |
| `externalResources.helpcenter.entries.userguides` | string |  |
| `externalResources.helpcenter.entries.welcomepage` | string |  |
| `externalResources.integrations.entries.drupal` | string |  |
| `externalResources.integrations.entries.pipedrive` | string |  |
| `externalResources.integrations.entries.wordpress` | string |  |
| `externalResources.integrations.entries.zapier` | string |  |
| `externalResources.integrations.entries.zoom` | string |  |
| `externalResources.site.domain` | string |  |
| `externalResources.site.entries.allconnectors` | string |  |
| `externalResources.site.entries.buydeveloper` | string |  |
| `externalResources.site.entries.buyenterprise` | string |  |
| `externalResources.site.entries.collaborationrooms` | string |  |
| `externalResources.site.entries.customrooms` | string |  |
| `externalResources.site.entries.demoorder` | string |  |
| `externalResources.site.entries.desktop` | string |  |
| `externalResources.site.entries.docspace` | string |  |
| `externalResources.site.entries.docspaceprices` | string |  |
| `externalResources.site.entries.downloaddesktop` | string |  |
| `externalResources.site.entries.downloadmobile` | string |  |
| `externalResources.site.entries.forenterprises` | string |  |
| `externalResources.site.entries.formfillingrooms` | string |  |
| `externalResources.site.entries.officeforandroid` | string |  |
| `externalResources.site.entries.officefordrupal` | string |  |
| `externalResources.site.entries.officeforios` | string |  |
| `externalResources.site.entries.officeforwordpress` | string |  |
| `externalResources.site.entries.officeforzapier` | string |  |
| `externalResources.site.entries.officeforzoom` | string |  |
| `externalResources.site.entries.openai` | string |  |
| `externalResources.site.entries.privaterooms` | string |  |
| `externalResources.site.entries.publicrooms` | string |  |
| `externalResources.site.entries.registrationcanceled` | string |  |
| `externalResources.site.entries.seamlesscollaboration` | string |  |
| `externalResources.site.entries.subscribe` | string |  |
| `externalResources.site.entries.wrongportalname` | string |  |
| `externalResources.socialNetworks.entries.facebook` | string |  |
| `externalResources.socialNetworks.entries.instagram` | string |  |
| `externalResources.socialNetworks.entries.tiktok` | string |  |
| `externalResources.socialNetworks.entries.twitter` | string |  |
| `externalResources.socialNetworks.entries.youtube` | string |  |
| `externalResources.support.domain` | string |  |
| `externalResources.support.entries.request` | string |  |
| `externalResources.videoguides.domain` | string |  |
| `externalResources.videoguides.entries.activesessions` | string |  |
| `externalResources.videoguides.entries.archive` | string |  |
| `externalResources.videoguides.entries.backup` | string |  |
| `externalResources.videoguides.entries.createfiles` | string |  |
| `externalResources.videoguides.entries.fileversions` | string |  |
| `externalResources.videoguides.entries.filterfiles` | string |  |
| `externalResources.videoguides.entries.full` | string |  |
| `externalResources.videoguides.entries.hotkeys` | string |  |
| `externalResources.videoguides.entries.operationswithfiles` | string |  |
| `externalResources.videoguides.entries.playlist` | string |  |
| `externalResources.videoguides.entries.profile` | string |  |
| `externalResources.videoguides.entries.roles` | string |  |
| `externalResources.videoguides.entries.rooms` | string |  |
| `externalResources.videoguides.entries.security` | string |  |
| `externalResources.videoguides.entries.whatis` | string |  |
| `firebase.apiKey` | string |  |
| `firebase.appId` | string |  |
| `firebase.authDomain` | string |  |
| `firebase.databaseURL` | string |  |
| `firebase.measurementId` | string |  |
| `firebase.messagingSenderId` | string |  |
| `firebase.projectId` | string |  |
| `firebase.storageBucket` | string |  |
| `formGallery.domain` | string |  |
| `formGallery.ext` | string |  |
| `formGallery.path` | string |  |
| `formGallery.uploadDashboard` | string |  |
| `formGallery.uploadDomain` | string |  |
| `formGallery.uploadExt` | string |  |
| `formGallery.uploadPath` | string |  |
| `greetingSettings` | string |  |
| `invitationLimit` | number |  |
| `isAmi` | boolean |  |
| `limitedAccessDevToolsForUsers` | boolean |  |
| `limitedAccessSpace` | boolean |  |
| `logoText` | string |  |
| `maxImageUploadSize` | number |  |
| `nameSchemaId` | string |  |
| `ownerId` | string |  |
| `plugins.delete` | boolean |  |
| `plugins.enabled` | boolean |  |
| `plugins.upload` | boolean |  |
| `recaptchaType` | number |  |
| `socketUrl` | string |  |
| `standalone` | boolean |  |
| `tagManagerId` | string |  |
| `tenantAlias` | string |  |
| `tenantStatus` | number |  |
| `timezone` | string |  |
| `trustedDomainsType` | number |  |
| `userNameRegex` | string |  |
| `utcHoursOffset` | number |  |
| `utcOffset` | string |  |
| `version` | string |  |
| `zendeskKey` | string |  |

## Native endpoint

Through the native ONLYOFFICE DocSpace API, this operation is `GET /api/2.0/settings` (base URL `https://docspace-t0dtrp.onlyoffice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-settings.md) for the provider-specific parameters and requirements.

