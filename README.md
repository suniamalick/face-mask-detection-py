# Face Mask Detection System - FYP Prototype

**Project Title:** Face Mask Detection System  
**Group ID:** F25PROJECT188B3  
**Author:** BC210400872  
**Supervisor:** Madiha Faqir Hussain
**GitRepo:** https://github.com/suniamalick/face-mask-detection-py

---

## 📁 Project Files

### Jupyter Notebooks:
1. **`face_mask_detection_training.ipynb`** - Local Jupyter version
2. **`face_mask_detection_training_colab.ipynb`** - Google Colab version ⭐ RECOMMENDED

### Documentation:
3. **`QUICK_START_GUIDE.md`** - Quick setup instructions
4. **`COLAB_DOWNLOAD_GUIDE.md`** - How to download results from Colab
5. **`setup_instructions.md`** - Detailed local installation guide
6. **`requirements.txt`** - Python dependencies

### Dataset:
7. **`dataset/`** folder with:
   - `with_mask/` - 690 images
   - `without_mask/` - 686 images
   - **Total: 1,376 images** (perfectly balanced)

---

## 🚀 Quick Start (2 Minutes)

### Use Google Colab (EASIEST):

1. **Zip your dataset:**
   - Right-click `dataset` folder → Send to → Compressed folder
   - Creates `dataset.zip`

2. **Open Google Colab:**
   - Go to: https://colab.research.google.com/
   - Upload `face_mask_detection_training_colab.ipynb`

3. **Enable GPU:**
   - Runtime → Change runtime type → GPU → Save

4. **Run everything:**
   - Runtime → Run all (Ctrl+F9)
   - Upload `dataset.zip` when prompted
   - Wait 2-3 minutes

5. **Get results:**
   - `face_mask_detection_results.zip` downloads automatically
   - Contains model + all graphs + metrics

---

## 📊 What You'll Get

After training, the `training_results/` folder contains:

### 1. Trained Model
- **`facemask_model.h5`** (~6-10 MB)
- Ready for deployment or inference
- Load with: `tf.keras.models.load_model('facemask_model.h5')`

### 2. Visualizations (High-Quality PNG)
- **`training_history.png`** - Accuracy & loss curves (for report)
- **`sample_images.png`** - 10 dataset samples (for dataset section)
- **`data_augmentation.png`** - Augmentation examples (for methodology)

### 3. Data Files
- **`training_metrics.csv`** - Epoch-by-epoch data (Excel-ready)
- **`model_summary.txt`** - Model architecture details
- **`RESULTS_SUMMARY.txt`** - Complete training report

---

## 🎯 Expected Performance

Based on your 1,376 image dataset:

- **Validation Accuracy:** 90-96% (typically 93-95%)
- **Training Time (GPU):** 2-3 minutes
- **Training Time (CPU):** 10-15 minutes
- **Model Size:** ~6-10 MB

---

## 📝 For FYP Submission

### Required Deliverables (All Included):

✅ **Code:** Jupyter notebook with complete implementation  
✅ **Dataset Loading:** TensorFlow utilities, 80/20 split  
✅ **Preprocessing:** Resize (224×224), normalize, augmentation  
✅ **CNN Model:** 3 Conv blocks, pooling, dense, dropout  
✅ **Training:** Binary crossentropy, Adam, 15 epochs  
✅ **Visualizations:** Sample images, training curves  
✅ **Evaluation:** Final validation metrics  
✅ **Model Saving:** Saved as `facemask_model.h5`  
✅ **Academic Comments:** Viva-ready explanations  

### For Your Report:

Include these sections with corresponding files:

1. **Introduction** - Project overview
2. **Dataset** - Use `sample_images.png`
3. **Methodology** 
   - Show `data_augmentation.png`
   - Explain CNN architecture
4. **Implementation** - Include code snippets from notebook
5. **Results**
   - Use `training_history.png`
   - Reference `RESULTS_SUMMARY.txt`
6. **Conclusion** - Discuss accuracy and future improvements

### For Viva Defense:

Be ready to explain:
- Why CNN for image classification?
- What does each layer do? (Conv2D, MaxPooling, Dense, Dropout)
- Why data augmentation? (Prevent overfitting, improve generalization)
- Why binary crossentropy? (Binary classification loss function)
- Why Adam optimizer? (Adaptive learning rate)
- How to interpret accuracy/loss curves?

---

## 🛠️ Technical Specifications

**Architecture:**
- Input: 224×224×3 RGB images
- 3 Convolutional blocks (32, 64, 128 filters)
- MaxPooling after each conv block
- Flatten + Dense (128) + Dropout (0.5)
- Output: Sigmoid activation (binary)

**Training:**
- Optimizer: Adam (lr=0.001)
- Loss: Binary Crossentropy
- Epochs: 15
- Batch Size: 32
- Data Split: 80% train, 20% validation

**Augmentation:**
- Random Rotation (±20%)
- Random Horizontal Flip
- Random Zoom (±10%)

---

## 🆘 Troubleshooting

### Issue: Download doesn't start in Colab
**Solution:** 
- Check popup blockers
- Or manually download from file panel (📁 icon on left)
- Or use individual download cell

### Issue: Training takes too long
**Solution:**
- Verify GPU is enabled (Runtime → Change runtime type)
- Should take 2-3 min with GPU, not 20+ min

### Issue: Out of memory error
**Solution:**
- Reduce batch size from 32 to 16
- Or reduce image size from 224 to 128

### Issue: Accuracy is low (<80%)
**Solution:**
- Increase epochs from 15 to 25-30
- Check if dataset loaded correctly
- Verify class balance

---

## 📧 Next Steps

After downloading:

1. **Extract zip file** to get `training_results/` folder
2. **Verify all 7 files** are present (see checklist in COLAB_DOWNLOAD_GUIDE.md)
3. **Include in FYP report:**
   - Notebook (PDF or HTML export)
   - Visualizations
   - Results summary
4. **Prepare for viva** using the saved metrics and model summary

---

## 🎓 Academic Notes

This prototype demonstrates:
- **Machine Learning Pipeline:** Complete end-to-end implementation
- **Deep Learning:** CNN for image classification
- **Data Engineering:** Loading, preprocessing, augmentation
- **Model Evaluation:** Proper train/val split, metrics visualization
- **Reproducibility:** Fixed seeds, documented parameters

Target FYP grade: This implementation covers all core requirements for a strong ML prototype submission.

---

**Good luck with your FYP! 🎉**
