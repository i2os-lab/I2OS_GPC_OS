# v7.3M vs v7.3N Comparison

| Category | v7.3M | v7.3N |
|---|---|---|
| Core role | Entry recovery version | Initial-move verification version |
| Main behavior | Enters when structure is sufficiently aligned | Enters only after real favorable movement |
| Strength | Restored actual entries | Suppressed weak entries |
| Weakness | Entered post-rebound flat structures | Very selective / low frequency |
| Typical failure | max_fav near 0 → early cut | Entry does not occur unless movement confirms |
| Key added filter | EntryQualityGate relaxation | Initial Move Confirmation Guard |
| Main new condition | none | fav_pips, dFlow, pulse, trigger votes |
| Best use | Confirm that entry pipeline works | Filter for true GO quality |
| System stage | “Can enter” | “Can wait” |
| OS layer emphasis | Execution recovery | Reality Module |

## Structural Meaning

```text
v7.3M:
Structure aligned → entry

v7.3N:
Structure aligned
→ candidate survives
→ real movement appears
→ entry
```

## Practical Interpretation

v7.3M proved that the EA could enter again after over-filtering.

v7.3N proved that the EA could suppress weak entries and wait for real initial movement.

## Design Conclusion

v7.3N should not be relaxed globally.  
If tuning becomes necessary, only a localized Reality or FlowNotRising parameter should be adjusted.