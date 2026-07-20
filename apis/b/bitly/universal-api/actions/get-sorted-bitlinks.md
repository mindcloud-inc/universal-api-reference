# Bitly: Get Sorted Bitlinks

Retrieves sorted bitlinks for a group in Bitly.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-sorted-bitlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-sorted-bitlinks?connectionId=$CONNECTION_ID&groupGuid=string&sort=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupGuid": "string",
  "sort": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-sorted-bitlinks?${params}`, {
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
| `groupGuid` | string | yes |  |
| `size` | number | no |  |
| `sort` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        {
          "archived": true,
          "campaignIds": [
            "https://example.com"
          ],
          "clientId": "https://example.com",
          "createdAt": "https://example.com",
          "createdBy": "https://example.com",
          "customBitlinks": [
            "https://example.com"
          ],
          "deeplinks": [
            {
              "appGuid": "https://example.com",
              "appUriPath": "https://example.com",
              "bitlink": "https://example.com",
              "brandGuid": "https://example.com",
              "created": "https://example.com",
              "guid": "https://example.com",
              "installType": "https://example.com",
              "installUrl": "https://example.com",
              "modified": "https://example.com",
              "os": "https://example.com"
            }
          ],
          "expirationAt": "https://example.com",
          "id": "https://example.com",
          "launchpadIds": [
            "https://example.com"
          ],
          "link": "https://example.com",
          "longUrl": "https://example.com",
          "qrCodeIds": [
            "https://example.com"
          ],
          "tags": [
            "https://example.com"
          ],
          "title": "https://example.com"
        }
      ],
      "sortedLinks": [
        {
          "clicks": 1,
          "id": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links[].archived` | boolean |  |
| `links[].campaignIds` | array<string> |  |
| `links[].clientId` | string |  |
| `links[].createdAt` | string |  |
| `links[].createdBy` | string |  |
| `links[].customBitlinks` | array<string> |  |
| `links[].deeplinks[].appGuid` | string |  |
| `links[].deeplinks[].appUriPath` | string |  |
| `links[].deeplinks[].bitlink` | string |  |
| `links[].deeplinks[].brandGuid` | string |  |
| `links[].deeplinks[].created` | string |  |
| `links[].deeplinks[].guid` | string |  |
| `links[].deeplinks[].installType` | string |  |
| `links[].deeplinks[].installUrl` | string |  |
| `links[].deeplinks[].modified` | string |  |
| `links[].deeplinks[].os` | string |  |
| `links[].expirationAt` | string |  |
| `links[].id` | string |  |
| `links[].launchpadIds` | array<string> |  |
| `links[].link` | string |  |
| `links[].longUrl` | string |  |
| `links[].qrCodeIds` | array<string> |  |
| `links[].tags` | array<string> |  |
| `links[].title` | string |  |
| `sortedLinks[].clicks` | number |  |
| `sortedLinks[].id` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /groups/:group_guid/bitlinks/:sort` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sorted-bitlinks.md) for the provider-specific parameters and requirements.

