# MCP Prompts (SSE)

This project exposes two MCP prompts over SSE for a mobile client.

## Prompts

- `essay-lecture`: 生成作文材料的深度思辨与写作指导HTML讲义
  - args: `cover_title`, `material_text`
- `essay-grading`: 生成高考作文阅卷与批改的完整HTML报告
  - args: `material_text`, `student_essay`

## Run locally

```bash
npm install
npm start
```

## Auth

Set one or more tokens (comma-separated). If unset, auth is disabled.

```bash
MCP_AUTH_TOKENS=token1,token2
```

Clients should send:

```
Authorization: Bearer <token>
```

## MCP endpoint

```
GET  /mcp
POST /mcp?sessionId=...
```

## Zeabur deploy notes

- Build command: `npm install`
- Start command: `npm start`
- Set env: `MCP_AUTH_TOKENS` and (optional) `PORT`
- Use the public URL + `/mcp` in your mobile client
