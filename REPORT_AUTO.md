# TDSM v2 — AUTO REPORT

## 1. Overall metrics (at threshold=0.5)
### train
- Acc=0.9812 | Precision=0.9720 | Recall=0.9945 | F1=0.9831
- AUROC=0.9976 | AUPRC=0.9971
- Confusion=[[28562, 1038], [199, 36066]]

### val
- Acc=0.9795 | Precision=0.9693 | Recall=0.9944 | F1=0.9817
- AUROC=0.9969 | AUPRC=0.9958
- Confusion=[[7114, 286], [51, 9016]]

### test
- Acc=0.9809 | Precision=0.9715 | Recall=0.9945 | F1=0.9828
- AUROC=0.9975 | AUPRC=0.9969
- Confusion=[[35676, 1324], [250, 45082]]

## 2. Threshold optimization (test)
- Best threshold (max F1): **0.54**
- At best thr: Acc=0.9858 | P=0.9891 | R=0.9851 | F1=0.9871
- AUROC=0.9975 | AUPRC=0.9969
- Figures: `threshold_sweep.png`, `roc_test.png`, `pr_test.png`

## 3. Calibration
- ECE (quantile 15 bins): **0.330**
- Figure: `calibration_test.png`

## 4. Early-Exit
- delta=0.9, early_ratio_test=0.079%

## 5. Robustness (AutoAttack APGD-CE, L2)
- clean_acc=0.981
  - eps=0.05 → robust_acc=0.684
  - eps=0.10 → robust_acc=0.682
  - eps=0.15 → robust_acc=0.680
  - eps=0.20 → robust_acc=0.678
  - eps=0.25 → robust_acc=0.675
- Figure: `robust_curve.png`
