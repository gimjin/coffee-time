<div align="center">
  <h1>💬 Message MCP</h1>
  <p>
    🌐 다른 언어:
    <a href="README.md">English</a> |
    <a href="README.zh.md">中文</a> |
    <a href="README.ja.md">日本語</a>
  </p>
  <h3>데스크톱 알림, 이메일 및 API 푸시로 AI 작업 대기 불안을 줄이고 편안하게 커피 한잔을 즐기세요.</h3>
  <a href="#">
    <img src="https://badge.mcpx.dev?type=server" title="MCP Server"/>
  </a>
  <a href="https://deepwiki.com/gimjin/message-mcp">
    <img src="https://deepwiki.com/badge.svg" alt="Ask DeepWiki">
  </a>
  <a href="https://smithery.ai/server/@gimjin/message-mcp">
    <img src="https://smithery.ai/badge/@gimjin/message-mcp" alt="smithery badge">
  </a>
  <a href="https://github.com/gimjin/message-mcp/blob/main/.github/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/gimjin/message-mcp/ci.yml" alt="MIT License">
  </a>
  <a href="https://www.npmjs.com/package/message-mcp">
    <img src="https://img.shields.io/npm/v/message-mcp" alt="NPM Version">
  </a>
  <a href="https://github.com/gimjin/message-mcp/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/gimjin/message-mcp" alt="MIT License">
  </a>
</div>

## 🤔 아직도 이런 "감시식"으로 AI를 사용하고 계신가요?

걱정스러운 상사처럼 AI 출력을 한 줄씩 응시하며, 분명히 다른 일을 처리할 수 있음에도 불구하고 화면에서 잠시도 떨어질 수 없어 하고 있습니다.

**Message MCP로 완전히 주의력을 해방시켜 보세요!**

## 💡 사용법

[![인스톨_MCP-Cursor](https://img.shields.io/badge/인스톨_MCP-Cursor-171717)](https://cursor.com/install-mcp?name=message-mcp&config=eyJjb21tYW5kIjogIm5weCIsImFyZ3MiOiBbIm1lc3NhZ2UtbWNwQGxhdGVzdCJdfQ==) [![인스톨_MCP-VS_Code](https://img.shields.io/badge/인스톨_MCP-VS_Code-0098FF)](https://insiders.vscode.dev/redirect?url=vscode:mcp/install?{%22name%22:%22message-mcp%22,%22command%22:%22npx%22,%22args%22:[%22message-mcp@latest%22]}) [![인스톨_MCP-VS_Code_Insiders](https://img.shields.io/badge/인스톨_MCP-VS_Code_Insiders-24bfa5)](https://insiders.vscode.dev/redirect?url=vscode-insiders:mcp/install?{%22name%22:%22message-mcp%22,%22command%22:%22npx%22,%22args%22:[%22message-mcp@latest%22]})

🧑 **사용자**: 테트리스 웹 게임을 만들어 주세요. **_작업 완료 후 알려주세요_**.  
🤖 **AI**: 테트리스 게임을 만들기 시작하겠습니다...

> [!tip]
> `Cursor 설정 → Rules` 에 **_"작업 완료 후 알려주세요"_** 를 추가하여 반복적인 지시와 작별하세요.
> 또는 **_"복잡한 작업 완료 후 알려주세요"_** 를 추가하면, AI는 복잡한 작업에 대해서만 알려주고 간단한 작업은 방해하지 않습니다.

### 수동 설치

#### MacOS / Linux

```json
{
  "mcpServers": {
    "message-mcp": {
      "command": "npx",
      "args": ["message-mcp@latest"]
    }
  }
}
```

#### Windows

```json
{
  "mcpServers": {
    "message-mcp": {
      "command": "cmd",
      "args": ["/c", "npx", "message-mcp@latest"]
    }
  }
}
```

#### 이메일 알림 설정(선택)

이메일 알림을 사용하려면 `args` 배열에 SMTP URL을 추가하세요:

```json
{
  "mcpServers": {
    "message-mcp": {
      "command": "npx",
      "args": [
        "message-mcp@latest",
        "--smtp-url=smtp://user@gmail.com:pass@smtp.gmail.com:587"
      ]
    }
  }
}
```

**주요 SMTP URL 예시:**

- **Gmail**: `smtp://user:pass@smtp.gmail.com:587`
- **Outlook**: `smtp://user:pass@smtp-mail.outlook.com:587`
- **Yahoo**: `smtp://user:pass@smtp.mail.yahoo.com:587`
- **QQ메일**: `smtps://user:pass@smtp.qq.com:465`

#### 웹훅 알림 설정(선택)

웹훅 알림을 사용하려면 API URL을 추가하세요:

```json
{
  "mcpServers": {
    "message-mcp": {
      "command": "npx",
      "args": ["message-mcp@latest", "--api-url=https://httpbin.org/post"]
    }
  }
}
```

## 📌 시스템 요구사항

- Node.js: 18 이상
- macOS: 네이티브 알림은 10.8 이상 필요
- Linux: notify-osd 또는 libnotify-bin 설치 필요(Ubuntu는 기본 포함)
- Windows: 8 이상, 또는 8 미만은 작업 표시줄 풍선 알림

## ⚡ 문제 해결

#### Windows 시스템 알림이 비활성화됨

설정 > 알림 및 작업 > 앱 및 기타 발신자로부터 알림 받기 → 사용

#### WSL2 환경에서 OS 알림 누락

```bash
sudo find / -type f -name "snoretoast-*.exe" 2>/dev/null
/path/to/.../node_modules/snoretoast-x64.exe
/path/to/.../node_modules/snoretoast-x86.exe

chmod +x /path/to/.../node_modules/snoretoast-*.exe
```
