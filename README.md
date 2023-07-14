# Sentence Generation

This project focuses on completing incomplete sentences

## Models
There are two models in this project:
* LSTM (Along with other dense layers)
* Transformer (Not implemented currently)

## LSTM Model Architecture

The model is implemented using TensorFlow's Keras API. It consists of the following layers:

    Input Embedding Layer: An embedding layer that maps input tokens to dense vectors.
        Embedding size: 256
        Input length: max_seq_len - 1

    Dense Layers: A series of dense layers with ReLU activation functions.
        Dense layer 1: 1024 units
        Dense layer 1: 512 units
        Dense layer 2: 256 units
        Dense layer 3: 128 units
        Dense layer 4: 64 units
        Dense layer 5: 32 units
        Dense layer 6: 16 units
        Dense layer 7: 8 units
        Dense layer 8: 4 units
        Dense layer 9: 8 units
        Dense layer 10: 16 units
        Dense layer 11: 32 units
        Dense layer 12: 64 units
        Dense layer 13: 128 units
        Dense layer 14: 256 units
        Dense layer 15: 512 units
        Dense layer 16: 1024 units
        Dropout layer: 0.5 dropout rate

    LSTM Layer: A Long Short-Term Memory (LSTM) layer for sequence modeling.
        LSTM units: 1024
        Dropout layer: 0.5 dropout rate

    More Dense Layers: Two dense layers both with the ReLU activation functions.
        Dense layer 1: 256 units
        Dense layer 2: 128 units

    Output Layer: A dense layer with softmax activation for predicting the next word.
        Activation: softmax
        Output units: total_words

### Training

The LSTM model is trained using the following configurations:

    Loss function: Categorical Crossentropy
    Optimizer: Adam

### Sample Output

Here are some sample sentences generated by the LSTM model (Text in ** is the input):

    *I* Am Looking For Information In Cambridge Centre
    *Hi* Am Looking For Information Can You Help Me With A Place To Stay While Im In Town
    *My Address Is* Restaurants Rd The South Number Is Ejaop5Qe And You Try To Book It For You Cb20Qq
