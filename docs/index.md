## DLS

This page contains the database and interactive plots for ... paper. 

You can modify or add your paper information into the database trough a ***pull request***. 
To do so follow these steps:

1. Fork the [dl_seismology](https://github.com/smousavi05/dl_seismology)
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature'). You can use GitHub editor directly to change the CSV
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

 
### Database
You can find our database of DL-seismology paperes [here](https://github.com/smousavi05/dl_seismology/blob/main/docs/paper_test.csv)

This is an example of data struncture in our database:

```markdown
	{
		"ref": "Yang_2019_yang2019deep",
    "title": "Deep-learning inversion: A next-generation seismic velocity model building method",
    "journal": "Geophysics",
    "category": "Inverse Problems",
		"sub_category_I": "Active Seismology", 
		"sub_category_II": "Subsurface Characterization", 
		"task": ["Velocity Model Building"],
    "sub_task": "Prestack", 
		"ml_type": ["ANN"],
    "network_type": ["CNN"],
    "network_name": ["U-Net"],
    "architecture":[64, 64, 128, 128, 512, 512, 1024, 1024, 512, 512, 256, 256, 128, 128, 64],
    "training_process": ["Supervised_Learning", "Transfer_Learning"],
		"inputs": ["multishot gathers"],
    "outputs": ["predicted velocity model"],
    "data_domain": ["time"],
		"data_type": ["synthetic"],
    "data_size": [1600],		
		"performance_metrice": [],
    "performance_score": [],
    "baseline": ["FWI"],
		"notes": "The main contribution of this paper is the use of U-Net. The prediction in the model space has dimensions of 201# 301; interestingly, the spatial                  dimensions of the input coincide with the second spatial dimension of the predictions, which is basically the number of receivers per shot. The U-                Net architecture on the encoder side is composed by 10 2D convolutional layers interleaved with batch normalization and using ReLU as the                        activation function. For connecting layers, every two 2D convolutional layers are placed between the encoder and decoder. The decoder section is                  composed of eight 2D convolutional layers and interleaved with the corresponding deconvolution layers. The ADAM optimizer is using during                        training, with two different numbers of epochs, depending on which data set is used as input, learning rate, and batch size constant. Results are                presented as the comparison between the CNN predictions and a MS-FWI solver, for which the starting model is a smoothed version of the ground                    truth. The first set of results (for a CNN trained with synthetic data) presented is competitive with FWI solutions; the salt bodies are                         identified and properly placed, but the boundaries are less continuous than the FWI solution, as can observed in Figure 12(c)."
	},
 ```

### ML-Seismology Glossary

You can find an updating glossary of seismological tasks and relevant machine learning techniques [here](https://smousavi05.gitbook.io/mlseismology/)

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/smousavi05/dl_seismology/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
