# Flux-DRaFT
DRaFT RL technique for Flux.

Will update code once I'm done hyperparameter tuning. Based on the paper: https://arxiv.org/abs/2309.17400

Questions:
1. Can I train a lora on schnell and have it work on dev ?
2. Can I overfit the reward and use a low lora scale during inference ? Will that preserve the base capabilities well enough ?
3. What reward models work best ?
4. What hyperparameters work ?


Bugs encountered:
1. Torch compile fails when peft transformer layers are set to only transformer blocks. Only single blocks work, all q,k,v layers from all blocks work. Error seems to come from
   flash attn. Weird. Haven't debugged in detail.
   
