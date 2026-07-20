# Every.org: Get Nonprofit

Retrieves details about a nonprofit from Every.org.

```
GET https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-nonprofit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Every.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-nonprofit?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-nonprofit?${params}`, {
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
| `identifier` | string | yes | A nonprofit slug, EIN, or nonprofit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nonprofit": {
        "coverImageCloudinaryId": "string",
        "coverImageUrl": "https://example.com",
        "description": "string",
        "descriptionLong": "string",
        "disbursementType": "string",
        "donationsEnabled": true,
        "ein": "string",
        "hasAdmin": true,
        "id": "string",
        "locationAddress": "string",
        "locationLatLng": {
          "coordinates": [
            1
          ],
          "type": "string"
        },
        "logoCloudinaryId": "string",
        "logoUrl": "https://example.com",
        "name": "Ava Chen",
        "nteeCode": "string",
        "nteeCodeMeaning": {
          "decileCode": "string",
          "decileMeaning": "string",
          "majorCode": "string",
          "majorMeaning": "string"
        },
        "primarySlug": "string",
        "profileUrl": "https://example.com",
        "websiteUrl": "https://example.com"
      },
      "nonprofitTags": [
        {
          "causeCategory": "string",
          "id": "string",
          "tagImageCloudinaryId": "string",
          "tagImageUrl": "https://example.com",
          "tagName": "Ava Chen",
          "tagUrl": "https://example.com",
          "title": "string"
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
| `nonprofit.coverImageCloudinaryId` | string |  |
| `nonprofit.coverImageUrl` | string |  |
| `nonprofit.description` | string |  |
| `nonprofit.descriptionLong` | string |  |
| `nonprofit.disbursementType` | string |  |
| `nonprofit.donationsEnabled` | boolean |  |
| `nonprofit.ein` | string |  |
| `nonprofit.hasAdmin` | boolean |  |
| `nonprofit.id` | string |  |
| `nonprofit.locationAddress` | string |  |
| `nonprofit.locationLatLng.coordinates[]` | number |  |
| `nonprofit.locationLatLng.type` | string |  |
| `nonprofit.logoCloudinaryId` | string |  |
| `nonprofit.logoUrl` | string |  |
| `nonprofit.name` | string |  |
| `nonprofit.nteeCode` | string |  |
| `nonprofit.nteeCodeMeaning.decileCode` | string |  |
| `nonprofit.nteeCodeMeaning.decileMeaning` | string |  |
| `nonprofit.nteeCodeMeaning.majorCode` | string |  |
| `nonprofit.nteeCodeMeaning.majorMeaning` | string |  |
| `nonprofit.primarySlug` | string |  |
| `nonprofit.profileUrl` | string |  |
| `nonprofit.websiteUrl` | string |  |
| `nonprofitTags[].causeCategory` | string |  |
| `nonprofitTags[].id` | string |  |
| `nonprofitTags[].tagImageCloudinaryId` | string |  |
| `nonprofitTags[].tagImageUrl` | string |  |
| `nonprofitTags[].tagName` | string |  |
| `nonprofitTags[].tagUrl` | string |  |
| `nonprofitTags[].title` | string |  |

## Native endpoint

Through the native Every.org API, this operation is `GET /nonprofit/:identifier` (base URL `https://partners.every.org/v0.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nonprofit.md) for the provider-specific parameters and requirements.

