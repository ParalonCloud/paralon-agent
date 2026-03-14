# Paralon Agent for Mac

Native macOS agent for [ParalonCloud](https://paraloncloud.com) — earn points by sharing your Apple Silicon GPU for AI inference.

## Requirements

- macOS with Apple Silicon

Ollama is installed automatically if not already present.

## Quick Start

1. Go to [paraloncloud.com/dashboard](https://paraloncloud.com/dashboard#provide-compute)
2. Create a new node and select **Apple Silicon** as the node type
3. Copy and run the launch command from the dashboard

The agent will install as a background service, start automatically, and run on login.

## Commands

paralon-agent status      Check if agent is running and connected
paralon-agent logs        Follow live agent logs
paralon-agent stop        Stop the background agent
paralon-agent start       Start the background agent
paralon-agent uninstall   Stop and remove background service
paralon-agent version     Show version
paralon-agent help        Show help


## How It Works

1. The agent connects to ParalonCloud and reports your hardware specs
2. When a model is assigned, it automatically downloads and serves it via Ollama
3. Inference requests are routed to your machine and you earn points
4. The agent auto-updates silently when a new version is available (checks every 5 minutes)

## Logs

Logs are stored in `~/.paralon/paralon-agent.log` and automatically rotated.

## Uninstall

```bash
paralon-agent uninstall
This stops the agent and removes it from startup. To fully clean up:


rm -rf ~/.paralon
