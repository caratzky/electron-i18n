# powerMonitor

> Отслеживает изменения состояния питания устройства.

Process: [Main](../glossary.md#main-process)

You cannot require or use this module until the `ready` event of the `app` module is emitted.

Например:

```javascript
const electron = require('electron')
const {app} = electron

app.on('ready', () => {
  electron.powerMonitor.on('suspend', () => {
    console.log('The system is going to sleep')
  })
})
```

## События

The `powerMonitor` module emits the following events:

### Событие: 'suspend'

Emitted when the system is suspending.

### Событие: 'resume'

Emitted when system is resuming.

### Событие: 'on-ac' *Windows*

Emitted when the system changes to AC power.

### Событие: 'on-battery' *Windows*

Emitted when system changes to battery power.