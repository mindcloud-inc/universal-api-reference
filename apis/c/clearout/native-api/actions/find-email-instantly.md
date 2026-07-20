# Find Email Instantly with Clearout

Finds contact email addresses in Clearout instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_finder/instant`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Find Email Instantly](https://docs.clearout.io/developers/api/email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the person (eg:- Mr. Tony Stark or Robert Downey Jr.) |
| `domain` | body | `string` | yes | Domain or Company name (eg:- marvel.com or Marvel Entertainment Company) |
| `timeout` | body | `number` | no | Request wait time (in milliseconds) |
| `queue` | body | `boolean` | no | Flag to indicate whether email discovery can be performed in background even after the request timed out, this will help to retrieve result later using queue id or downloaded from Clearout App -> My Activities. Setting 'false' will stop the email discovery immediately when timeout occured |
