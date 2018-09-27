#This is a basic seq2seq model made using tensorflow library to understand the working of the concept.

The model is given input and trained to predict the same sequence.

First : 
		The input is batched i.e. input = [[5, 7, 8], [6, 3], [3], [1]] 
		The padded input will make equal size array of each input instance
		batched_input = 
						array([[5, 6, 3, 1],
							   [7, 3, 0, 0],
							   [8, 0, 0, 0]], dtype=int32
							   
							   
							   
Next : 
		Given encoder_inputs [5, 6, 7], decoder_targets would be [5, 6, 7, 1],where 1 is for EOS, and decoder_inputs would be [1, 5, 6, 7] - decoder_inputs are lagged by 1 step, passing previous token as input at current step.