# Guess Email with Toofr

Guesses a prospect's email address in Toofr.

## Endpoint

- **Method:** `POST`
- **Path:** `/guess_email.json`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [Guess Email](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_name` | query | `string` | yes | Person company name or domain. |
| `first_name` | query | `string` | yes | Person first name. |
| `last_name` | query | `string` | yes | Person last name. |
