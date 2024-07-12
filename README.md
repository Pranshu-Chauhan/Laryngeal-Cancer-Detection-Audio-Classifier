# Laryngeal Audio Classification

## Dataset
- **Source:** [Saarland University SimmDB](https://simmdb.coli.uni-saarland.de/index.php4#target)
- **Description:** Male dataset, ages 42-75, vowel /a/ including neutral pitch, high pitch, low pitch, and low-high-low pitch variations.
  
| Classes            | Gender | No. of People | Total Samples |
|--------------------|--------|---------------|---------------|
| Healthy            | Male   | 37            | 148           |
| Laryngeal Cancer   | Male   | 21            | 84            |

*Note: Testing with female data was not possible due to insufficient samples.*

## Results
### Preprocessing Techniques and Features Used

- **Time Stretching + Time Masking + Frequency Masking**
- Features: MFCC, Chroma, Mel-Spectrogram, Spectral Contrast, Tonnetz, Zero Crossing Rate

### Classification Methods and Accuracy on the /a/ vowel dataset

| Method                        | Accuracy |
|-------------------------------|----------|
| Logistic Regression           | 97.85%   |
| Random Forest Classifier      | 96.77%   |
| Support Vector Classifier     | 94.62%   |
| SincNet + DNN                 | 99.14%   |
| SincNet + DNN (with Resampling)| 89.67%   |
| SincNet + DNN (MFCC only)     | 96.5%    |
| DNN (MFCC only)               | 100%     |

### Additional Tests
- SincNet model tested separately on /i/, /u/ vowel data with specific results.

| Method                        | Accuracy |
|-------------------------------|----------|
| SincNet + DNN (/i/ vowel)     | 69.7%   |
| SincNet + DNN (/u/ vowel)     | 69.8%   |

## Usage
1. **Clone Repository:**
   ```bash
   git clone https://github.com/your-username/laryngeal-audio-classification.git
   cd laryngeal-audio-classification
   ```
   
2. **Setup Environment:**
   - Install Jupyter Notebook and required dependencies (NumPy, SciPy, TensorFlow, etc.).

3. **Open Notebooks:**
   - Explore and run the Jupyter Notebook files in `scripts/` for data processing, training, and evaluation.
   ```bash
   jupyter notebook
   ```

4. **Review Results:**
   - Examine outputs and visualizations within the notebooks for detailed analysis and performance evaluation.

## Contributing
- Contributions are welcome! Fork the repository and submit pull requests for improvements or new features.

## License
- This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
