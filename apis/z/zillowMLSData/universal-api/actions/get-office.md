# Zillow MLS Data: Get office

Retrieves a specific office from Zillow MLS Data.

```
GET https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-office
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow MLS Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-office?connectionId=$CONNECTION_ID&dataset=string&officeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "string",
  "officeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-office?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code that contains the office. |
| `officeId` | string | yes | Office identifier from the Bridge dataset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "FranchiseAffiliation": "string",
      "ModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "OfficeAddress1": "string",
      "OfficeBranchType": "string",
      "OfficeCity": "string",
      "OfficeEmail": "ava@example.com",
      "OfficeKey": "string",
      "OfficeMlsId": "string",
      "OfficeName": "Ava Chen",
      "OfficePhone": "string",
      "OfficePostalCode": "string",
      "OfficeStateOrProvince": "string",
      "OfficeStatus": "string",
      "OfficeType": "string",
      "OriginatingSystemName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BridgeModificationTimestamp` | date | Last Bridge-side modification timestamp. |
| `FranchiseAffiliation` | string | Office franchise affiliation. |
| `ModificationTimestamp` | date | Last office modification timestamp. |
| `OfficeAddress1` | string | Office street address. |
| `OfficeBranchType` | string | Office branch type. |
| `OfficeCity` | string | Office city. |
| `OfficeEmail` | string | Office email address. |
| `OfficeKey` | string | Primary office key. |
| `OfficeMlsId` | string | MLS office identifier. |
| `OfficeName` | string | Office name. |
| `OfficePhone` | string | Office phone number. |
| `OfficePostalCode` | string | Office postal code. |
| `OfficeStateOrProvince` | string | Office state or province. |
| `OfficeStatus` | string | Office status. |
| `OfficeType` | string | Office type. |
| `OriginatingSystemName` | string | Originating system name. |

## Native endpoint

Through the native Zillow MLS Data API, this operation is `GET /:dataset/offices/:officeId` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-office.md) for the provider-specific parameters and requirements.

