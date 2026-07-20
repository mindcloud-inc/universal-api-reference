# Klipfolio: Get Data Source

Retrieves a data source from Klipfolio by ID.

```
GET https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klipfolio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-data-source?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-data-source?${params}`, {
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
| `datasourceId` | string | no | The Klipfolio datasource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "connector": "string",
      "created_by": "string",
      "date_created": "string",
      "date_last_refresh": "string",
      "description": "string",
      "disabled": true,
      "format": "string",
      "id": "string",
      "in_progress": true,
      "is_dynamic": true,
      "is_locked": true,
      "isDataFeed": true,
      "name": "Ava Chen",
      "product_family": 1,
      "refresh_interval": 1,
      "serviceProviderPublicId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | The company that owns the datasource. |
| `connector` | string | The datasource connector type. |
| `created_by` | string | The user ID that created the datasource. |
| `date_created` | string | Datasource creation timestamp. |
| `date_last_refresh` | string | Most recent refresh timestamp. |
| `description` | string | The datasource description. |
| `disabled` | boolean | Whether the datasource is disabled. |
| `format` | string | The datasource data format. |
| `id` | string | The datasource ID. |
| `in_progress` | boolean | Whether a datasource job is in progress. |
| `is_dynamic` | boolean | Whether the datasource is dynamic. |
| `is_locked` | boolean | Whether the datasource is locked. |
| `isDataFeed` | boolean | Whether the datasource is a data feed. |
| `name` | string | The datasource name. |
| `product_family` | number | Klipfolio product family code. |
| `refresh_interval` | number | Refresh interval in seconds. |
| `serviceProviderPublicId` | string | The public ID of the backing service provider. |

## Native endpoint

Through the native Klipfolio API, this operation is `GET /datasources/:datasourceId` (base URL `https://app.klipfolio.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-source.md) for the provider-specific parameters and requirements.

