# Deploy this Streamlit project

The screenshot error occurs because `model.pkl` is missing beside `app.py` in the deployed repository. Keep **all** the contents of this package together at the repository root:

```
app.py
model.pkl
scaler.pkl
metrics.json
requirements.txt
assets/network_cover.png
```

Do not upload only `app.py`, and do not leave the files inside an unextracted ZIP in the repository. On Streamlit Community Cloud, set the main file path to `app.py` and redeploy after committing all files. The app displays a specific missing-file message if the package is incomplete.

For a local check after installing `requirements.txt`, run `streamlit run app.py` from this directory. The saved model and scaler were built with scikit-learn 1.8.0, which is pinned in `requirements.txt`.
