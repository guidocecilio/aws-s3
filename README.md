# aws-s3
This is a master repo for AWS S3 tests specially for S3 Object Upload

## s3upload.py
This is a fork of the code example provided by K Hung in his article
[AWS: S3 (SIMPLE STORAGE SERVICE) IV - UPLOADING A LARGE FILE](https://www.bogotobogo.com/DevOps/AWS/aws_S3_uploading_large_file.php)
The code shows how to upload long files to an AWS S3 Bucket.

Requirements
------------

To install and run these examples you need:

- Python 2.7 or 3.3+
- virtualenv (not required if you are using Python 3.4)
- git (only to clone this repository)

Installation
------------

The commands below set everything up to run the examples:

    $ git clone git@github.com:guidocecilio/aws-s3.git 
    $ cd aws-s3
    $ virtualenv .env
    $ . .env/bin/activate
    (.env) pip install -r requirements.txt

Note for Python 3.4 users: replace `virtualenv` with `pyvenv`.

Note for Microsoft Windows users: replace the virtual environment activation command above with `.env\Scripts\activate`.

Application requirements
------------------------

Because S3 requires AWS keys, we should provide our keys: *AWS_ACCESS_KEY* and *AWS_ACCESS_SECRET_KEY*. The code example uses them as variables from the OS Enviroment. e.g: /etc/boto.conf or ~/.boto:

```sh
[Credentials]
AWS_ACCESS_KEY_ID = A...3
AWS_SECRET_ACCESS_KEY = W...9
```

If you are _The Impatient_ and knows your AWS credentials, just define the variables from the terminal and run the CLI tool. e.g:

```sh
$ export AWS_ACCESS_KEY_ID=xxxxxxxxxxxxxxxxxxxxxxxxxxxx
$ export AWS_ACCESS_SECRET_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxx
$ python s3upload.py -b guidocecilio-test-big-files -f recipes.csv
```

Usage
-----

```sh
$ python s3upload.py -b bucket-name -f file-name
```



