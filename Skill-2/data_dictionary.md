# Data Dictionary - Cleaned One Piece Bounty Dataset

| Column | Type | Meaning |
|---|---|---|
| Rank | Int | Competition rank by bounty (ties share a rank). Empty when bounty is unknown |
| Name | Text | Character name, whitespace-normalised and unique |
| Bounty_Berry | Int | Bounty in Berries. Empty when unknown (never imputed) |
| Bounty_Billions | Float | Bounty divided by 1e9, for readable axes |
| Bounty_Log10 | Float | log10 of Bounty_Berry, tames the heavy right skew |
| Bounty_Known | Bool | False when the source said Unknown |
| Currency_Fixed | Bool | True when the source used a non-Berry currency symbol that was corrected |
| Bounty_Outlier | Bool | True when Bounty_Log10 lies outside the IQR fences |

Dropped: Source_Rank (S.no), because it was rebuilt from the bounty itself and carried 999 placeholders.
