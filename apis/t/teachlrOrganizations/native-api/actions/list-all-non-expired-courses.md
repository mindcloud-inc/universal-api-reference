# List All Non-Expired Courses with Teachlr Organizations

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/all`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [List All Non-Expired Courses](https://soporte.teachlr.com/base-de-conocimientos/listar-los-cursos-de-una-escuela-usando-el-api-de-teachlr-organizaciones/)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Word or phrase to match against course title, headline, or description. |
| `sort` | query | `string` | no | Course attribute to sort by, such as created_at or title. |
| `ord` | query | `string` | no | Sort direction: asc or desc. |
