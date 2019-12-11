## About

Segments texts, extracts weighed keywords, conducts a synonym set walk for every possible keyword pair and stores the calculated distances.

Parts of this research project will happen inside [Colaboratory](https://colab.research.google.com/drive/1iGL_J01I-SAtw2HG8uoJMLgYhYqMzzAK) as well.


## Segmenting

We segment documents in order to increase the accuracy of the sysnonymity scoring.

A simple CLI tool  [cmd/cli/segmenter.go](cmd/cli/segmenter.go) which is using [github.com/jdkato/prose](https://github.com/jdkato/prose) is user for the first steps of segmenting.

To run it simply provide your string as first argument:

```bash
go run cmd/segmenter/*.go "Hello darkness my old friend"
```

## Argument Analysis API

We extract and weigh keywords, conduct sysnonym set walks and store the calculated disctances. For a detailed API documentation, please refer to the APIBlueprint located in [apiary.apib](apiary.apib) or check out the interactive docs at [Apiary](https://argumentanalysisresearch.docs.apiary.io/#).

## License

### General

Find the corresponding license attached in [LICENSE](LICENSE).
This project is meant for experimenting which means using and vendoring in foreign code where suitable.
This license does only applies to code written by contributors, external libraries can differ and got their licenses stored in the respective vendor directory.

### Code for ADW

The licensing from the original project applies without any changes.

>ADW (Align, Disambiguate and Walk) -- A Unified Approach for Measuring Semantic Similarity.
>
>Copyright (c) 2014 Sapienza University of Rome.
>All Rights Reserved.
>
>This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY;
>without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
>
>If you use this system, please cite the following paper:
>
>> M. T. Pilehvar, D. Jurgens and R. Navigli. Align, Disambiguate and Walk: A Unified Approach for Measuring Semantic Similarity.
>> Proceedings of the 51st Annual Meeting of the Association for Computational Linguistics (ACL 2013), Sofia, Bulgaria, August 4-9, 2013, pp. 1341-1351.

### Code for wrapping around ADW

The code for wrapping around the ADW implementation is licensed through the same [LICENSE](LICENSE) as the original library.

Thanks to the respective authors and developers for providing their work.
