# Track Lead with PIMMS

Creates a new tracked lead event in PIMMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/track/lead`
- **Base URL:** `https://api.pimms.io`
- **Official documentation:** [Track Lead](https://pimms.apidocumentation.com/reference#tag/track/POST/track/lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clickId` | body | `string` | yes | Unique identifier for the click event in PIMMS, typically retrieved from the 'pimms_id' browser cookie for accurate attribution. |
| `eventName` | body | `string` | yes | Name of the specific lead or conversion event you want to track (e.g., 'Sign up', 'Free Trial Registration'). |
| `externalId` | body | `string` | no | A unique identifier from your internal system (such as user ID) to link customer journeys across platforms. |
| `customerName` | body | `string` | no | Optional customer name, useful for personalized reporting and CRM integrations. |
| `customerEmail` | body | `string` | no | Customer email address to enhance CRM synchronization and facilitate personalized marketing efforts. |
| `customerAvatar` | body | `string` | no | URL to the customer's avatar image, used for richer user profiles in integrated CRM or analytics platforms. |
| `metadata` | body | `object` | no | Additional structured data or context about the lead event, aiding advanced segmentation and reporting. |
