# Natural Language Processing course resources
https://www.coursera.org/learn/language-processing

## Running on Google Colab
Google has released its own flavour of Jupyter called Colab, which has free GPUs!

Here's how you can use it:
1. Sign into your Google account
2. Open https://colab.research.google.com
3. Click **GITHUB** tab, paste https://github.com/hse-aml/natural-language-processing and press Enter
4. Choose the notebook you want to open, e.g. week1/week1-MultilabelClassification.ipynb
5. Click **File -> Save a copy in Drive...** to save your progress in Google Drive
6. _If you need a GPU_, click **Runtime -> Change runtime type** and select **GPU** in Hardware accelerator box
7. Execute the following code in the first cell:
```python
! wget https://raw.githubusercontent.com/hse-aml/natural-language-processing/master/setup_google_colab.py -O setup_google_colab.py
import setup_google_colab
setup_google_colab.setup_week1()  # change to the week you're working on
```
8. If you run many notebooks on Colab, they can continue to eat up memory,
you can kill them with `! pkill -9 python3` and check with `! nvidia-smi` that GPU memory is freed.

**Known issues:**
* No support for `ipywidgets`, so we cannot use fancy `tqdm` progress bars.
For now, we use a simplified version of a progress bar suitable for Colab.
* Blinking animation with `IPython.display.clear_output()`.
It's usable, but still looking for a workaround.

## Running elsewhere

[AWS](AWS-tutorial.md)

[Docker](Docker-tutorial.md)
