# HMM-Hidden-Markov-Models

	1 
		Implement the functions forward() and backward() in hmm.py:
		• forward(π, A, B,O) takes the model parameters π, A, B and the observation sequence O as input
		  and output a numpy array α, where α[j, t − 1] = P(Zt = sj, X1:t = x1:t). Note that this is α[j, t − 1]
		  instead of α[j, t] just because the index of an array starts from 0.
		• backward(π, A, B,O) takes the model parameters π, A, B and the observation sequence O as input
		  and output a numpy array β, where β[j, t − 1] = P(Xt+1:N = xt+1:N | Zt = sj). Note the same index
		  difference.

	2 
		Calculate P(X1:N = O) from the output of your forward and backward algorithms. Implement the function seqprob_forward() 
	and seqprob_backward() in hmm.py. Both of them should return P(X1:N = O). Note that in seqprob_forward() the input is only 
	the forward messages, while in seqprob backward() you have access to the model parameters too.

	3 
		Find the most likely state path based on the observation O, namely,
			argmax z∗ 1:N P(Z1:N = z∗ 1:N | X1:N = O).
		Implement the Viterbi algorithm viterbi() in hmm.py. The function viterbi(π, A, B,O) takes
	the model parameters π, A, B and the observation sequence O as inputs and outputs a list path which contains
	the most likely state path z∗ 1:N (in terms of the state index) you have found.