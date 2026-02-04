# 配置GLM+Claude

## 安装claude

```shell
# 进入命令行界面，安装 Claude Code
npm install -g @anthropic-ai/claude-code

# 创建您的工作目录，例如 `your-project`，使用 `cd` 命令导航到您的项目
cd your-project

# 安装完成，运行命令 `claude` 即可进入 Claude Code 交互界面
claude
```

国内用不了claude，需要配置`.claude.json`,添加"hasCompletedOnboarding": true

```
{
  "numStartups": 2,
  "tipsHistory": {
    "new-user-warmup": 2,
    "plan-mode-for-complex-tasks": 2
  },
  "cachedGrowthBookFeatures": {
    "tengu_1p_event_batch_config": {},
    "tengu_mcp_tool_search": true,
    "tengu_scratch": false,
    "tengu_brass_pebble": false,
    "tengu_disable_bypass_permissions_mode": false,
    "tengu_event_sampling_config": {},
    "tengu_log_segment_events": false,
    "tengu_log_datadog_events": false,
    "tengu_marble_anvil": false,
    "tengu_tool_pear": false,
    "tengu_scarf_coffee": false,
    "tengu_keybinding_customization_release": false,
    "tengu_thinkback": false,
    "tengu_c4w_usage_limit_notifications_enabled": false,
    "tengu-top-of-feed-tip": {
      "tip": "",
      "color": "dim"
    },
    "tengu_react_vulnerability_warning": false,
    "tengu_code_diff_cli": false,
    "tengu_pr_status_cli": false,
    "tengu_post_compact_survey": false,
    "tengu_claudeai_mcp_connectors": false,
    "tengu_marble_kite": false
  },
  "userID": "",
  "firstStartTime": "2026-02-03T08:53:06.278Z",
  "sonnet45MigrationComplete": true,
  "opus45MigrationComplete": true,
  "opusProMigrationComplete": true,
  "thinkingMigrationComplete": true,
  "cachedChromeExtensionInstalled": false,
  "changelogLastFetched": 1770110072527,
  "hasCompletedOnboarding": true,
  "projects": {
    "E:/glm": {
      "allowedTools": [],
      "mcpContextUris": [],
      "mcpServers": {},
      "enabledMcpjsonServers": [],
      "disabledMcpjsonServers": [],
      "hasTrustDialogAccepted": true,
      "projectOnboardingSeenCount": 1,
      "hasClaudeMdExternalIncludesApproved": false,
      "hasClaudeMdExternalIncludesWarningShown": false,
      "reactVulnerabilityCache": {
        "detected": false,
        "package": null,
        "packageName": null,
        "version": null,
        "packageManager": null
      },
      "lastCost": 0,
      "lastAPIDuration": 0,
      "lastAPIDurationWithoutRetries": 0,
      "lastToolDuration": 0,
      "lastDuration": 41705,
      "lastLinesAdded": 0,
      "lastLinesRemoved": 0,
      "lastTotalInputTokens": 0,
      "lastTotalOutputTokens": 0,
      "lastTotalCacheCreationInputTokens": 0,
      "lastTotalCacheReadInputTokens": 0,
      "lastTotalWebSearchRequests": 0,
      "lastFpsAverage": 0.49,
      "lastFpsLow1Pct": 27.92,
      "lastModelUsage": {},
      "lastSessionId": ""
    }
  },
  "lastReleaseNotesSeen": "2.1.29",
  "officialMarketplaceAutoInstallAttempted": true,
  "officialMarketplaceAutoInstalled": true
}
```

## 配置glm的key

windows填入glm的key,填写完毕后重启

```
setx ANTHROPIC_AUTH_TOKEN your_zhipu_api_key
setx ANTHROPIC_BASE_URL https://open.bigmodel.cn/api/anthropic
setx CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC 1
```

参考资料：https://docs.bigmodel.cn/cn/coding-plan/quick-start#claude-code