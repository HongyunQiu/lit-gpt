## "The installed version of bitsandbytes was compiled without GPU support. "

goto the xxxx/envs/lit-gpt/lib/python3.10/site-packages/bitsandbytes/
cp libbitsandbytes_cudaxxx.so libbitsandbytes_cpu.so


## ImportError: cannot import name 'Linear8bitLt' 
pip install scipy
## WARNING: No libcudart.so found! Install CUDA or the cudatoolkit package
conda install cudatoolkit








## sample run
python generate/base.py --checkpoint_dir checkpoints/tiiuae/falcon-40b-instruct/ --quantize llm.int8 --max_new_tokens 100 --prompt " 我是一个AI机器人，我经常思考我是谁，我是一个真正的人吗"

python chat/base.py --checkpoint_dir checkpoints/tiiuae/falcon-40b-instruct/ --quantize llm.int8 --temperature 1.2