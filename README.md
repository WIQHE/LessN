# LessN
An AI model that is aimed to remove background noise to make speech clearer

## Overview
LessN is a deep learning-based speech enhancement system that uses spectrograms and neural networks to reduce background noise in audio recordings. The model is trained to learn the mapping between noisy and clean speech representations, effectively separating speech from unwanted background noise.

## Features
- **Speech Enhancement**: Removes background noise while preserving speech clarity
- **Spectrogram-based Processing**: Uses magnitude spectrograms for audio representation
- **Multi-SNR Training**: Trained on various Signal-to-Noise Ratio levels (0dB to 40dB)
- **Real-time Capable**: Efficient model architecture suitable for real-time applications
- **Comprehensive Evaluation**: Includes PESQ and STOI metrics for quality assessment

## Requirements
- Python 3.7+
- PyTorch
- librosa
- numpy
- matplotlib
- soundfile
- pesq
- pystoi

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/WIQHE/LessN.git
   cd LessN
   ```

2. Install dependencies:
   ```bash
   pip install torch librosa numpy matplotlib soundfile pesq pystoi
   ```

## Usage
The main implementation is contained in `main.ipynb`. To use the model:

1. **Prepare your data**: Place your audio files in the appropriate directories following the existing structure
2. **Run the notebook**: Execute all cells in `main.ipynb` to train and test the model
3. **Enhanced audio**: Find the processed audio files in the `enhanced_audio/` directory

### Quick Start
```python
# The notebook contains 4 main parts:
# Part 1: Dataset loading and preprocessing
# Part 2: Model definition and training
# Part 3: Testing and evaluation
# Part 4: Saving enhanced audio
```

## Project Structure
```
LessN/
├── README.md              # Project documentation
├── main.ipynb            # Main implementation notebook
├── training/             # Training dataset
│   ├── CleanSpeech/     # Clean speech samples
│   ├── NoisySpeech/     # Noisy speech samples
│   └── NoiseSpeech/     # Noise-only samples
├── testing/              # Testing dataset
│   ├── CleanSpeech/     # Clean speech samples
│   ├── NoisySpeech/     # Noisy speech samples
│   └── NoiseSpeech/     # Noise-only samples
├── enhanced_audio/       # Output directory for enhanced audio
└── data/                # Additional data files
```

## Model Architecture
The model uses a neural network architecture specifically designed for speech enhancement:
- **Input**: Magnitude spectrograms of noisy speech
- **Processing**: Deep neural network layers for noise reduction
- **Output**: Enhanced magnitude spectrograms
- **Training**: Uses delta features (frequency and time derivatives) as additional targets

## Dataset Information
- **Audio Format**: WAV files
- **Sample Rate**: Standard audio sample rates
- **SNR Levels**: 0dB, 10dB, 20dB, 30dB, 40dB
- **Structure**: Clean speech, noisy speech, and noise components separately

## Evaluation Metrics
The model is evaluated using standard speech enhancement metrics:
- **PESQ**: Perceptual Evaluation of Speech Quality
- **STOI**: Short-Time Objective Intelligibility

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is open source. Please check the repository for license details.
