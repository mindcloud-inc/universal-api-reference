# Fetch LinkedIn profile information (GET) with ConnectSafely

Retrieve detailed profile information for a LinkedIn member via query parameters. Same functionality as POST /profile but using GET method for simpler integration. Results are cached for 6 hours. **Rate limit: 120 unique profiles per day per LinkedIn account (cached requests do not count against limit).**

## Endpoint

- **Method:** `GET`
- **Path:** `/profile`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Fetch LinkedIn profile information (GET)](https://connectsafely.ai/docs/api/linkedin-profiles/get-profile-get-profile)

## Quota

120 unique profile fetches per day per LinkedIn account. Cached profiles (within 6 hours) do not count against limit.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | query | `string` | yes | LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123") |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `includeGeoLocation` | query | `boolean` | no | Include detailed geo location data Default: `False`. |
| `includeContact` | query | `boolean` | no | Include contact info if visible Default: `False`. |
| `forceRefresh` | query | `boolean` | no | Skip cache and fetch fresh data Default: `False`. |

### Example response

```json
{
  "success": true,
  "profileId": "anandi-devi",
  "accountId": "696ce9e780e0483585e4e553",
  "profile": {
    "firstName": "Anandi",
    "lastName": "Devi",
    "headline": "Go-To-Market (GTM) Engineer @ ConnectSafely | MBA",
    "entityUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
    "publicIdentifier": "anandi-devi",
    "isPremium": true,
    "isConnected": true,
    "connectionDegree": "DISTANCE_1"
  }
}
```

## Error status codes

`400`, `401`. Bodies follow the shared `{ success, code, message }` error shape.
