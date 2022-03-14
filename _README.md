# Write Markdown, Get a Keptn Shipyard File

This is self-contained tool. It runs entirely in the browser (JavaScript based). No data ever leaves your browser.

`https://agardnerit.github.io/markdown-shipyard-creator/`

## Usage

See page or denote:

- Stages with a single hash: `# stage1`
- Sequences with a double hash: `## sequence1`
- Tasks with triple hashes: `### task1`

### Sequence triggeredOn

Either an unconditional trigger: `triggered on dev.delivery.finished`:

```
## sequence1
triggeredOn=dev.delivery.finished
```
or a conditional trigger: `triggered on dev.delivery.finished when evaluation.result=fail`:

```
## sequence1
triggeredOn=dev.delivery.finished,evaluation.result=fail
```

### Task Properties

Denoted with four hashes `#### key=value`:
```
...
### task1
#### deliverystrategy=blue_green_service
```

### Task triggeredAfter
A task can be `triggeredAfter` a certain amount of time: `triggeredAfter=10m`:

```
### task1
triggeredAfter=10m
```
