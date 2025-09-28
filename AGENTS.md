# ESPHome Configuration Agent Guidelines

## Build Commands
- Validate config: `esphome config <yaml-file>`
- Compile: `esphome compile <yaml-file>`
- Upload firmware: `esphome upload <yaml-file>`
- Run all steps: `esphome run <yaml-file>`
- Dashboard: `esphome dashboard config/`

## Code Style Guidelines
1. Use YAML anchor/alias (`&` and `*`) for reusable configurations
2. Use packages (`!include`, `!include_dir_named`) for modular configs
3. Follow naming scheme: `<location>-<purpose>.<area>.<room>.yaml`

## Configuration Standards
- IDs: Use lowercase with underscores, must be unique
- Pins: Always use internal GPIO numbers (e.g., GPIO16) or board aliases
- Time values: Use appropriate suffixes (ms, s, min, h)
- Indentation: 2 spaces

## Components Organization
- Group packages by type (sensor, switch, etc.)
- Use substitutions for reusable values
- Keep secrets in packages/common/secrets.yaml
- Use board-specific configs in boards/ directory

## Best Practices
- Document non-obvious configurations
- Use standard component structure from ESPHome docs
- Validate configuration before uploading
