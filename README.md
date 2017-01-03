## Language Identification
This iPython notebook builds and trains a deep model in Keras to predict languages based on lines of text. For now, the scope is restricted to programming languages since the required syntax is much more strict.

### Data
For programming languages, we use large codebases for each language. Namely,

* Python: [Django](https://github.com/django/django)
* Java: [Java off-heap cache](https://github.com/snazy/ohc)
* C: [FreeBSD](https://github.com/freebsd/freebsd)
* C++: [Caffe](https://github.com/BVLC/caffe)

To add/modify a language or its configuration for this model, you need only modify the `Config` cell in the notebook. You may use any suitably (~10,000s of lines, depending on language complexity) large codebases for each language. Set the `CODE_DIRS` dictionary to point at the root directories of these repos. The notebook will retrieve all of the desired code from the repos and use it as data.