# Instagram Poetry Generator
This project involves generating poetry using a Recurrent Neural Network (RNN) like a Bidirectional Long-Short Term Memory (LSTM) architecture model trained on 
the posts of a random Instagram poet. The project involved four main stages:

  1. ### Web Scraping : 
      The first step was to scrape the posts of a random Instagram poet using the Beautiful Soup API and then downloaded the posts using  urllib.request. 
      The posts were then saved as images in a local directory.

  2. ### OCR : 
      Next, I used Tesseract OCR to extract the text from the saved images, this text can then be used to train the RNN model. 
      The Tesseract OCR came in handy as it is an open-source OCR engine with good accuracy and support for multiple languages. 
      Tesseract OCR required its own preprocessing steps:
        1. **Image Cleaning:**
        The input image should be cleaned to remove any noise, smudges or other artifacts that may affect the accuracy of OCR. This can be done by applying image filters such as Gaussian blur, Median filter, or Adaptive Thresholding.

        2. **Image Binarization:**
        Tesseract OCR works best with binary images, where the text is in black and the background is white. Therefore, it is important to binarize the input image before running it through Tesseract OCR. This can be done using various techniques such as Thresholding, Otsu's Binarization, or Adaptive Thresholding.

        3. **Image Scaling:**
        The size of the input image can also affect the accuracy of OCR. If the image is too small, the text may not be legible, while if it is too large, the OCR engine may take longer to process it. Therefore, it is important to scale the image to an appropriate size before running it through Tesseract OCR.

        4. **Text Localization:**
        In some cases, the input image may contain multiple blocks of text, such as in a document or a webpage. In such cases, it is important to localize the text and extract the relevant portion before running it through Tesseract OCR. This can be done using techniques such as Bounding Box detection or Contour detection.
  
  3. ### Preprocessing and Tokenizing: 
      Once the text was stripped from the posts into a text file, basic preprocessing like removing special characters, numbers, extra information , etc. was done for Tokenization followed by creating Ngrams of the text data. 
     
  4. ### Model Training: 
      I built an RNN model using TensorFlow to generate poetry. The model was trained on the now tokenized Ngrams. The model's architecture includes
      an embedding layer in the size of the vocabulary, a bidirectional LSTM and a densely connected layer. 

## Depedencies
This project requires the following dependencies:

- Python 3.x
- TensorFlow 2.x
- Tesseract OCR
- NumPy
- Beautiful Soup 4
- urllib

You can install these dependencies using pip.
```
pip install tensorflow pytesseract numpy beautifulsoup4 urllib
```

## Results
After training for 400 epochs, the model reached an accuracy of 97.5% on the test set. Accuracy and Loss plots can be found in the Jupyter Notebooks. 

## Notes
Although the model reached high accuracy and very minimal loss, 
- The model can be made more complex, maybe transfer learning can be applied (eg: BERT)
- Synthetic data can be generated using the same model to increase training data.
- Tweak hyperparameters better
- The text generation logic can be improved for brevity
