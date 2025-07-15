# Roku Parrot Model

This is my parrot model + patterns + model history notes.

A parrot model should be trained and specific to your own voice, so I only recommend this for reference.

## Sounds (14)

### Non-linguistic sounds (4)
- pop
- cluck
- tut
- palate

### Linguistic sounds (10)
- ah
- oh
- guh
- eh
- nn
- ee
- er
- t
- sh
- ss

### Negative sounds (2)
- background - moving mic around, breathing, AC, table bumps, keyboard presses, door closing, adjusting things on the table, sitting in chair
- cough - throat clears, cough, nose clear, etc.

## Testing

Use [Parrot Tester](https://github.com/rokubop/parrot_tester) tool for testing your parrot model.

## parrot_integration.py
Made one change from the original, for grace thresholds to work.

Old:
```python
throttles = {}
if 'throttle' in pattern:
    if name not in pattern['throttle']:
        pattern['throttle'][name] = 0
    throttles = pattern['throttle']
```

New:
```python
throttles = {}
if 'throttle' in pattern:
    # if name not in pattern['throttle']:
    #     pattern['throttle'][name] = 0
    throttles = pattern['throttle']
```

You can check the [Parrot Tester](https://github.com/rokubop/parrot_tester) tool README for more information on this.