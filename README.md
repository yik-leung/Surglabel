# Surglabel 🩺

An annotation software specially designed for labeling surgical videos.

The two annotation tools previously mentioned in the ProstaTD project have now been merged into this single, unified annotation software. We have deliberately avoided adding AI features, as most of our workflow revolves around doctors correcting raw AI predictions. The tool is kept intentionally lightweight, since overly complex features often make doctors reluctant to use it (based on my practical experience).

## ✨ Features

- Single image annotation support: rectangle & polygon, with attribute editing (triplets, track ID, image-level tags, etc.)
- Batch annotation based on segmentation / bbox instances
- Batch annotation across different separation groups that belong to the same instance
- Many shortcuts and UI hints optimized after extensive feedback from doctors (e.g. highlight selected elements)
- Highly customizable settings for colors, line styles, label display, etc.
- When the same instances appear at the same time, they will be sorted by different coordinate orders to assist batch annotation
- Also supports batch annotation by track ID
- …and more

→ For more features and detailed instructions, please click the Help button in the menu.

## 🚀 Installation

### Option 1: Windows (Zero Installation)

Just download the latest `surglabel.exe` and double-click to run.

### Option 2: pip install (Windows / Ubuntu / macOS)

```bash
git clone https://github.com/yik-leung/Surglabel.git
cd Surglabel
pip install -r requirements.txt
python main.py
```

## 📼 Quick Start & Demo

<p align="center">
  <video src="https://github.com/user-attachments/assets/9cfae53a-a627-424f-b3b0-32ab38a50d8a" alt="Surglabel Demo" width="800"></video>
</p>

This demo video only shows a small fraction of what Surglabel can actually do. In real use, it actually supports batch-annotating thousands of frames quickly or segmentation instances....

For complete hotkeys, all available modes, tips & tricks, and detailed usage instructions →  please click the Help button in the top menu after launching the software.

## ⚠️ Current Limitations

Because the merging of two tools was done under time pressure, some parts remain quite specialized/customized. Future updates may address these problems.

For example:
- Image files in a folder **must be named with consecutive natural numbers**  
  (✅ Currently support format: `1.jpg`, `2.jpg`, `3.jpg`, …)
  
  (❌ May cause bugs format   : `00001.jpg`, `00002.jpg`, `frame_001.jpg`, etc.) 
- Some very specific workflows are still tuned to our internal projects

If you run into any bugs, unexpected behavior, or have suggestions for improvement, please feel free to open an issue on GitHub or email me directly.

## 🙏 Acknowledgments

- Core annotation logic heavily inspired by [labelme](https://github.com/wkentaro/labelme)

## 📄 Citation

If you find Surglabel helpful in your research or projects, please consider citing the associated paper:

```bibtex
@article{chen2025prostatd,
  title     = {ProstaTD: Bridging Surgical Triplet from Classification to Fully Supervised Detection},
  author    = {Yiliang Chen and Zhixi Li and Cheng Xu and Alex Qinyang Liu and Ruize Cui and Xuemiao Xu and Jeremy Yuen-Chun Teoh and Shengfeng He and Jing Qin},
  journal   = {arXiv preprint arXiv:2506.01130},
  year      = {2025}
}
```

Since this tool has added a lot of task-specific features for various surgical annotation tasks, we'll add a citation for this tool in future publications when relevant.
