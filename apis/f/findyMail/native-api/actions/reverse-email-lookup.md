# Reverse Email Lookup with FindyMail

Finds contact details in FindyMail by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/search/reverse-email`
- **Base URL:** `https://app.findymail.com`
- **Official documentation:** [Reverse Email Lookup](https://www.findymail.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to look up. |
| `with_profile` | body | `boolean` | no | When true, include full profile enrichment; this uses 2 credits instead of 1. |
