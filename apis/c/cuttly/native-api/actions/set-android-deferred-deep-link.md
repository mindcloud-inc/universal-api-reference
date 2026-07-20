# Set Android Deferred Deep Link with Cutt.ly

Sets an Android deferred deep link for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Set Android Deferred Deep Link](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `destination` | query | `string` | yes | Android deep link or intent URL. |
| `package_id` | query | `string` | yes | Android application package identifier. |
