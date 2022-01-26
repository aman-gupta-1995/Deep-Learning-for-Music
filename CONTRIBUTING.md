# How To Contribute

Contributions are welcome!
Please submit you issues, pull requests, improvements and comments in British English.
You can look at the issues and help to solve them or you can add some missing articles as described below.

### Adding an article

Here are the steps to follow for adding one (or multiple) article:
1. Check that the article is not already in the [dl4m.bib](dl4m.bib) file.
2. Fork the repo.
3. Add the desired bib entry at the beginning of [dl4m.bib](dl4m.bib). Take care to fill all this field for each bib entry (if there is no information about a field please indicate it as `fieldName = {No}`):
    - Bib entry type (inproceedings, article, techreport, unpublished,...) (N.B.: Indicate arxiv article as @unpublished and if you know of a possible submission use `note = {Submitted to "NameOfJournalOrConference"}`)
    - Bib key (in the form AuthorlastnameYear, e.g. `Snow1999`
    - title (N.B.: Make sure the title is not written in all caps and that each word does not start with a capital letter.)
    - author (N.B.: Check that all authors in the pdf files are present in the bib author field and in the same order. Indeed automatic bib tools tend to mess up the order or to forget some authors.)
    - year
    - booktitle or journal
    - dataset (e.g. `dataset = {Inhouse & [Jamendo](http://www.mathieuramona.com/wp/data/jamendo/) & [RWC](https://staff.aist.go.jp/m.goto/RWC-MDB/)},`)
        1. provide the link to the dataset  
        2. if multiple dataset are used, insert a ` & ` between each dataset
    - architecture (if multiple architectures are used, insert a ` & ` between each of them, e.g. `archi = {CNN & VPNN},`)
    - link (HTML link to the pdf file)
    - task (if multiple tasks are performed, insert a ` & ` between each of them, e.g. `task = {SVS & SVD},`). Please refer to the acronyms listed in [acronyms.md](acronyms.md)
    - dataaugmentation (if used, the type of data augmentation technique, otherwise `No`)
    - pages (if available)
    - code (HTML link to the code if available, `No` instead)
    - learningrate (if given in the paper or the code, the learning rate, otherwise `No`)
    - framework (if given in the paper or the code, the framework, otherwise `No`)
    - reproducible (the reproducibility details of the paper and code)
    - activation (if given in the paper or the code, the activation function, otherwise `No`)
    - epochs (if given in the paper or the code, the number of epoch, otherwise `No`)
    - batch (if given in the paper or the code, the number of batch, otherwise `No`)
    - loss (if given in the paper or the code, the loss function, otherwise `No`)
    - layers (if given in the paper or the code, the number of layers, otherwise `No`)
    - dropout (if given in the paper or the code, the loss function, otherwise `No`)
    - momentum (if given in the paper or the code, the momentum, otherwise `No`)
    - gpu (if given in the paper or the code, the type and number of GPUs, otherwise `No`)
    - metric (if given in the paper or the code, the metric, otherwise `No`)
    - computationtime (if given in the paper or the code, the global computation time and per epoch, otherwise `No`)
    - dimension (if given in the paper or the code, the number of dimension, otherwise `No`)
    - optimizer (if given in the paper or the code, the optimize function, otherwise `No`)
    - input (if given in the paper or the code, the input type, otherwise `No`)
    - month (for conference paper only)
    - address (for conference paper only)
    - note (optional additional custom notes, if you feel you want to share a great detail you read or give your opinion)

    For ease of use you can copy and paste and fill the following lines:
    ```
    @inproceedings{Snow1999,
        activation = {},
        address = {},
        architecture = {},
        author = {},
        batch = {},
        booktitle = {},
        code = {},
        computationtime = {},
        dataaugmentation = {},
        dataset = {},
        dimension = {},
        dropout = {},
        epochs = {},
        framework = {},
        gpu = {},
        input = {},
        layers = {},
        learningrate = {},
        link = {},
        loss = {},
        metric = {},
        momentum = {},
        month = {},
        note = {},
        optimizer = {},
        pages = {},
        reproducible = {},
        task = {},
        title = {},
        year = {},
    }
    ```
4. Check that you have installed this python package:
    1. numpy
    2. matplotlib
    3. bibtexparser
5. Launch the python script `python dl4m.py`.
6. Submit your pull request!

### Missing or incorrect field for an article

Thanks for spotting it! You can:
1. Submit an issue or
2. Make a pull request:
    1. Fork the repo.
    2. Add or update the corresponding field in [dl4m.bib](dl4m.bib).
    3. Launch the python script `python dl4m.py`.
    4. Submit your pull request with this title: `[Update][<bib_key>] field added or updated`, e.g. `[Update][Snow1999] added task`.

### Note

I am looking for a way to display relations between articles automatically like a mindmap. Tell me if you know anything able to handle that.
