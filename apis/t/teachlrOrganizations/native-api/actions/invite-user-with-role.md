# Invite User With Role with Teachlr Organizations

## Endpoint

- **Method:** `POST`
- **Path:** `/invite`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Invite User With Role](https://soporte.teachlr.com/base-de-conocimientos/invitar-un-usuario-a-una-escuela-con-un-rol-usando-el-api-de-teachlr-organizaciones/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the user to invite to the Teachlr school. |
| `role` | body | `number` | yes | Role to assign to the invited user. Teachlr accepts integer values from 2 to 4. |
