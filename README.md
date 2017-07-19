# Pokemon GAN

Pokemon Generative model using DCGAN from PyTorch examples. 

Experiments
- [ ] Default 50 epoch / 100 z-layer
- [ ] 100 epoch 
- [ ] 200 epoch
- [ ] 50 epoch / 200 z-layer
- [ ] Adapted training with additional "false" images. (i.e. Anime pics that are not pokemon)

## Run

mkdir -p results/output_ep100_z100
main.py --dataset folder --dataroot data/ --cuda --niter 100 --outf results/output_ep100_z100

mkdir -p results/output_ep200_z100
main.py --dataset folder --dataroot data/ --cuda --niter 200 --outf results/output_ep200_z100

mkdir -p results/output_ep50_z200
main.py --dataset folder --dataroot data/ --cuda --niter 50 -nz 200 --outf results/output_ep50_z200



## Usage
```
usage: main.py [-h] --dataset DATASET --dataroot DATAROOT [--workers WORKERS]
               [--batchSize BATCHSIZE] [--imageSize IMAGESIZE] [--nz NZ]
               [--ngf NGF] [--ndf NDF] [--niter NITER] [--lr LR]
               [--beta1 BETA1] [--cuda] [--ngpu NGPU] [--netG NETG]
               [--netD NETD]

optional arguments:
  -h, --help            show this help message and exit
  --dataset DATASET     cifar10 | lsun | imagenet | folder | lfw
  --dataroot DATAROOT   path to dataset
  --workers WORKERS     number of data loading workers
  --batchSize BATCHSIZE
                        input batch size
  --imageSize IMAGESIZE
                        the height / width of the input image to network
  --nz NZ               size of the latent z vector
  --ngf NGF
  --ndf NDF
  --niter NITER         number of epochs to train for
  --lr LR               learning rate, default=0.0002
  --beta1 BETA1         beta1 for adam. default=0.5
  --cuda                enables cuda
  --ngpu NGPU           number of GPUs to use
  --netG NETG           path to netG (to continue training)
  --netD NETD           path to netD (to continue training)
```
