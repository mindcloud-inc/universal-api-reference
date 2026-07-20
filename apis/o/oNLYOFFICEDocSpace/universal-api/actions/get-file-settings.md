# ONLYOFFICE DocSpace: Get File Settings

Retrieves file settings from ONLYOFFICE DocSpace.

```
GET https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-file-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ONLYOFFICE DocSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-file-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oNLYOFFICEDocSpace/latest/actions/get-file-settings?${params}`, {
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
      "automaticallyCleanUp": {
        "gap": 1,
        "isAutoCleanUp": true
      },
      "canSearchByContent": true,
      "chunkUploadSize": 1,
      "confirmDelete": true,
      "convertNotify": true,
      "defaultOrder": {
        "isAsc": true,
        "property": 1
      },
      "defaultSharingAccessRights": [
        1
      ],
      "displayFileExtension": true,
      "downloadTarGz": true,
      "enableThirdParty": true,
      "externalShare": true,
      "externalShareSocialMedia": true,
      "extsArchive": [
        "string"
      ],
      "extsAudio": [
        "string"
      ],
      "extsConvertible": {},
      "extsDiagram": [
        "string"
      ],
      "extsDocument": [
        "string"
      ],
      "extsFilesVectorized": [
        "string"
      ],
      "extsImage": [
        "string"
      ],
      "extsImagePreviewed": [
        "string"
      ],
      "extsMediaPreviewed": [
        "string"
      ],
      "extsMustConvert": [
        "string"
      ],
      "extsPresentation": [
        "string"
      ],
      "extsSpreadsheet": [
        "string"
      ],
      "extsUploadable": [
        "string"
      ],
      "extsVideo": [
        "string"
      ],
      "extsWebCommented": [
        "string"
      ],
      "extsWebCustomFilterEditing": [
        "string"
      ],
      "extsWebEdited": [
        "string"
      ],
      "extsWebEncrypt": [
        "string"
      ],
      "extsWebPreviewed": [
        "string"
      ],
      "extsWebRestrictedEditing": [
        "string"
      ],
      "extsWebReviewed": [
        "string"
      ],
      "favoritesSection": true,
      "fileDownloadUrlString": "https://example.com",
      "fileRedirectPreviewUrlString": "https://example.com",
      "fileThumbnailUrlString": "https://example.com",
      "fileWebEditorExternalUrlString": "https://example.com",
      "fileWebEditorUrlString": "https://example.com",
      "fileWebViewerExternalUrlString": "https://example.com",
      "fileWebViewerUrlString": "https://example.com",
      "forcesave": true,
      "hideConfirmCancelOperation": true,
      "hideConfirmConvertOpen": true,
      "hideConfirmConvertSave": true,
      "hideConfirmRoomLifetime": true,
      "internalFormats": {
        "document": "string",
        "pdf": "string",
        "presentation": "string",
        "spreadsheet": "string"
      },
      "keepNewFileName": true,
      "masterFormExtension": "string",
      "maxUploadThreadCount": 1,
      "maxVectorizationFileSize": 1,
      "openEditorInSameTab": true,
      "paramOutType": "string",
      "paramVersion": "string",
      "recentSection": true,
      "storeForcesave": true,
      "storeOriginalFiles": true,
      "templatesSection": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automaticallyCleanUp.gap` | number |  |
| `automaticallyCleanUp.isAutoCleanUp` | boolean |  |
| `canSearchByContent` | boolean |  |
| `chunkUploadSize` | number |  |
| `confirmDelete` | boolean |  |
| `convertNotify` | boolean |  |
| `defaultOrder.isAsc` | boolean |  |
| `defaultOrder.property` | number |  |
| `defaultSharingAccessRights[]` | number |  |
| `displayFileExtension` | boolean |  |
| `downloadTarGz` | boolean |  |
| `enableThirdParty` | boolean |  |
| `externalShare` | boolean |  |
| `externalShareSocialMedia` | boolean |  |
| `extsArchive[]` | string |  |
| `extsAudio[]` | string |  |
| `extsConvertible` | object |  |
| `extsDiagram[]` | string |  |
| `extsDocument[]` | string |  |
| `extsFilesVectorized[]` | string |  |
| `extsImage[]` | string |  |
| `extsImagePreviewed[]` | string |  |
| `extsMediaPreviewed[]` | string |  |
| `extsMustConvert[]` | string |  |
| `extsPresentation[]` | string |  |
| `extsSpreadsheet[]` | string |  |
| `extsUploadable[]` | string |  |
| `extsVideo[]` | string |  |
| `extsWebCommented[]` | string |  |
| `extsWebCustomFilterEditing[]` | string |  |
| `extsWebEdited[]` | string |  |
| `extsWebEncrypt[]` | string |  |
| `extsWebPreviewed[]` | string |  |
| `extsWebRestrictedEditing[]` | string |  |
| `extsWebReviewed[]` | string |  |
| `favoritesSection` | boolean |  |
| `fileDownloadUrlString` | string |  |
| `fileRedirectPreviewUrlString` | string |  |
| `fileThumbnailUrlString` | string |  |
| `fileWebEditorExternalUrlString` | string |  |
| `fileWebEditorUrlString` | string |  |
| `fileWebViewerExternalUrlString` | string |  |
| `fileWebViewerUrlString` | string |  |
| `forcesave` | boolean |  |
| `hideConfirmCancelOperation` | boolean |  |
| `hideConfirmConvertOpen` | boolean |  |
| `hideConfirmConvertSave` | boolean |  |
| `hideConfirmRoomLifetime` | boolean |  |
| `internalFormats.document` | string |  |
| `internalFormats.pdf` | string |  |
| `internalFormats.presentation` | string |  |
| `internalFormats.spreadsheet` | string |  |
| `keepNewFileName` | boolean |  |
| `masterFormExtension` | string |  |
| `maxUploadThreadCount` | number |  |
| `maxVectorizationFileSize` | number |  |
| `openEditorInSameTab` | boolean |  |
| `paramOutType` | string |  |
| `paramVersion` | string |  |
| `recentSection` | boolean |  |
| `storeForcesave` | boolean |  |
| `storeOriginalFiles` | boolean |  |
| `templatesSection` | boolean |  |

## Native endpoint

Through the native ONLYOFFICE DocSpace API, this operation is `GET /api/2.0/files/settings` (base URL `https://docspace-t0dtrp.onlyoffice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-settings.md) for the provider-specific parameters and requirements.

