######  PRUNING TECHNIQUES
-------------------------------------------------------
What is pruning?
- A techniques of removing unimportant parameters(weights, biases,  acivations) of deep neural network.
--------------------------------------------------------
Why?
1. Reduction in storage.
2. speed-up during testing
--------------------------------------------------------

Types of pruning:
1. Weight pruning 
2. Neuron pruning 





Code Snippet to get the weight details of each layers:
----------------------------------------------------------

for layer in model.layers:
    print("===== LAYER: ", layer.name, " =====")
    if layer.get_weights() != []:
        weights = layer.get_weights()[0] #for weight
        biases = layer.get_weights()[1] #for biases
        print("weights:")
        print(weights)
        print("biases:")
        print(biases)
    else:
        print("weights: ", [])