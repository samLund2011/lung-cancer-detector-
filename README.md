# LungView — Lung Image Review Prototype

An educational, browser-based lung image review interface. It accepts chest-image uploads, performs local image-quality checks, combines user-entered risk factors into a transparent review-priority score, and produces an exportable summary.

## Important

This project is **not a medical device** and does not diagnose or rule out lung cancer. Its image analysis is a non-clinical heuristic demonstration, not a trained or validated radiology model. Real chest imaging must be reviewed by qualified clinicians.

## Run

```bash
python3 -m http.server 8090
```

Open `http://localhost:8090`.

No upload leaves the browser; processing is local to the page.

## CT nodule model

`Lung_Nodule_CT_Colab.ipynb` runs the official MONAI 3D lung-nodule detection bundle on a Google Colab GPU. The bundle is pretrained on LUNA16/LIDC-IDRI and exports possible-nodule locations as JSON. It does not determine malignancy or establish that a scan is healthy.
