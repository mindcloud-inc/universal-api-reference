# Socket: Export SPDX SBOM

Exports a Socket SBOM in SPDX format.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/export-spdx-sbom
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/export-spdx-sbom?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/export-spdx-sbom?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationInfo": {
        "created": "string",
        "creators": [
          "string"
        ]
      },
      "dataLicense": "string",
      "documentDescribes": [
        "string"
      ],
      "documentNamespace": "Ava Chen",
      "name": "Ava Chen",
      "packages": [
        {
          "checksums": [
            {}
          ],
          "description": "string",
          "downloadLocation": "string",
          "externalRefs": [
            {}
          ],
          "filesAnalyzed": true,
          "homepage": "string",
          "licenseDeclared": "string",
          "name": "Ava Chen",
          "packageFileName": "Ava Chen",
          "primaryPackagePurpose": "string",
          "sPDXID": "string",
          "versionInfo": "string"
        }
      ],
      "relationships": [
        {
          "relatedSpdxElement": "string",
          "relationshipType": "string",
          "spdxElementId": "string"
        }
      ],
      "sPDXID": "string",
      "spdxVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationInfo` | object |  |
| `creationInfo.created` | string |  |
| `creationInfo.creators` | array<string> |  |
| `dataLicense` | string |  |
| `documentDescribes` | array<string> |  |
| `documentNamespace` | string |  |
| `name` | string |  |
| `packages` | array<object> |  |
| `packages[]` | object |  |
| `packages[].checksums` | array<object> |  |
| `packages[].checksums[]` | object |  |
| `packages[].description` | string |  |
| `packages[].downloadLocation` | string |  |
| `packages[].externalRefs` | array<object> |  |
| `packages[].externalRefs[]` | object |  |
| `packages[].filesAnalyzed` | boolean |  |
| `packages[].homepage` | string |  |
| `packages[].licenseDeclared` | string |  |
| `packages[].name` | string |  |
| `packages[].packageFileName` | string |  |
| `packages[].primaryPackagePurpose` | string |  |
| `packages[].sPDXID` | string |  |
| `packages[].versionInfo` | string |  |
| `relationships` | array<object> |  |
| `relationships[]` | object |  |
| `relationships[].relatedSpdxElement` | string |  |
| `relationships[].relationshipType` | string |  |
| `relationships[].spdxElementId` | string |  |
| `sPDXID` | string |  |
| `spdxVersion` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/export/spdx/:id` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-spdx-sbom.md) for the provider-specific parameters and requirements.

