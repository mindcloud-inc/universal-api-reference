# Find Email with FindyMail

Finds a verified email in FindyMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/search/name`
- **Base URL:** `https://app.findymail.com`
- **Official documentation:** [Find Email](https://www.findymail.com/api/email-finder/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Full name of the person, for example John Doe. |
| `domain` | body | `string` | yes | Company domain, for example example.com. |
