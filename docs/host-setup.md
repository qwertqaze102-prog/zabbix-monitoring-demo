# Host setup notes (Linux agent)

## Minimal agent checks
- `system.cpu.util`
- `vm.memory.util`
- `vfs.fs.size[/,pused]`
- `agent.ping`

## Example trigger ideas
- Agent unreachable for 3 minutes → severity High
- CPU > 90% for 10 minutes → Warning
- Free disk < 10% → High

## Ops practice
1. Create host group `Linux servers`
2. Link template `Linux by Zabbix agent`
3. Configure media type / user for alerts
4. Test notification with "Test item"
