# List Events with Edusign

Retrieves events from Edusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [List Events](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | yes | Query param for pagination, starts at page "1" and displays events per page (default: 1) |
| `limit` | query | `string` | no | Maximum number of events to return per page (default and max: 1000) |
| `start` | query | `string` | no | Filter events starting from this date (format: YYYY-MM-DD, ISO 8601) |
| `end` | query | `string` | no | Filter events ending before this date (format: YYYY-MM-DD, ISO 8601) <br><strong>Note:</strong> When both start and end dates are provided, events will be filtered to include only those occurring within this date range. |
| `studentId` | query | `string` | no | Show only events assigned to this specific student (use internal Edusign student ID) |
| `professorId` | query | `string` | no | Show only events assigned to this specific professor (use internal Edusign professor ID) |
| `apiIds` | query | `string` | no | Filter events by external API IDs (JSON array as string, e.g., '["api1","api2"]') |
| `light` | query | `string` | no | When set to true, returns simplified event data with only id, name, apiId, and apiType fields for faster loading |
