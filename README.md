# Gemma 3 270M Implementation

## Instructions
1. install jupitor
```bash
python3 -m venv jupyter-env
source jupyter-env/bin/activate
pip install jupyter

```
2. To run in terminal
```bash
# run
nohup python3 gemma_3_270_laksiri.py > output.log 2>&1 &

# view status
cat output.log
ps aux | grep gemma_3_270_laksiri.py
# output
# ubuntu     31905 99.7  5.3 25177616 1730884 pts/0 Rl  10:34  10:50 python3 gemma_3_270_laksiri.py
# ubuntu     34050  0.0  0.0   7016  2432 pts/0    S+   10:44   0:00 grep --color=auto gemma_3_270_laksiri.py

# stop
kill <pid> # 31905

# check gpu usage
nvidia-smi
```

3. Run Jupyter Notebook
```bash
jupyter notebook

# Opens a browser at http://localhost:8888
# You can open/create .ipynb files there.
```

4. AWS Instance Details

- Select your AMI: Deep Learning OSS Nvidia Driver AMI GPU PyTorch 2.7 (Ubuntu 22.04)
- Select instance type: g4dn.2xlarge
- Select Storage: 100 GB
- Under Advanced details → Purchasing option, check **Request Spot Instance**.
- Then launch → this is often the easiest way.

## Reference
- [I pre-trained Gemma3 270M from scratch](https://www.youtube.com/watch?v=bLDlwcl6hbA)

