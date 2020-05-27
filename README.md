Generative Adversarial Networks
===============================

源码、原文PDF、论文翻译PDF：

"Generative Adversarial Networks." Ian J. Goodfellow, Jean Pouget-Abadie,
Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville,
Yoshua Bengio. ArXiv 2014.

We are an academic lab, not a software company, and have no personnel
devoted to documenting and maintaing this research code.
Therefore this code is offered with absolutely no support.
Exact reproduction of the numbers in the paper depends on exact
reproduction of many factors,
including the version of all software dependencies and the choice of
underlying hardware (GPU model, etc). We used NVIDA Ge-Force GTX-580
graphics cards; other hardware will use different tree structures for
summation and incur different rounding error. If you do not reproduce our
setup exactly you should expect to need to re-tune your hyperparameters
slight for your new setup.

>我们是一个学术实验室，而不是软件公司，没有专门的人员来记录和维护这个研究代码。因此，该代码是绝对不支持的。论文中数字的精确复制依赖于许多因素的精确复制，包括所有软件依赖的版本和底层硬件的选择(GPU模型等)。我们使用NVIDA Ge-Force GTX-580显卡;其他硬件将使用不同的树结构进行求和，并产生不同的舍入误差。如果您没有完全复制我们的设置，您应该预期需要重新调整您的超参数轻微为您的新设置。

Moreover, we have not integrated any unit tests for this code into Theano
or Pylearn2 so subsequent changes to those libraries may break the code
in this repository. If you encounter problems with this code, you should
make sure that you are using the development branch of Pylearn2 and Theano,
and use "git checkout" to go to a commit from approximately June 9, 2014.

>此外，我们还没有将此代码的任何单元测试集成到Theano中或者Pylearn2，因此对这些库的后续更改可能会破坏代码在这个库。如果您在这段代码中遇到问题，您应该确保你正在使用Pylearn2和Theano的开发分支，从2014年6月9日开始使用“git checkout”进行提交。

This code itself requires no installation besides making sure that the
"adversarial" directory is in a directory in your PYTHONPATH. If
installed correctly, 'python -c "import adversarial"' will work. You
must also install Pylearn2 and Pylearn2's dependencies (Theano, numpy,
etc.)

>这段代码本身不需要安装，只需确保“adversarial”目录位于您的python path目录中。如果安装正确，'python -c "import adversarial"将工作。您还必须安装Pylearn2和Pylearn2的依赖项(Theano、numpy等)。

parzen_ll.py is the script used to estimate the log likelihood of the
model using the Parzen density technique.

Call pylearn2/scripts/train.py on the various yaml files in this repository
to train the model for each dataset reported in the paper. The names of
*.yaml are fairly self-explanatory.

>parzen_ll.py使用Parzen density technique来确定模型的对数似然，在这个存储库中的各种yaml文件上调用pylearn2/scripts/train.py训练论文中每个数据集的模型。

***

补充：

基本概念和公式推导： https://blog.csdn.net/stalbo/article/details/79283399
