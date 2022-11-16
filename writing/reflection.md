# Contact Searching

Make sure that you delete all of the markers and the written prompts
from this document. You should also ensure that the document does not have any
mistakes in spelling, grammar, or the syntax of Markdown. Ultimately, the final
version of your reflection should be a polished document that is suitable for
publication on your web site.

## Anthony Vazquez

## Program Output

### What is the output from running the following commands?

- `poetry run contactsearcher --job-description "engineer" --contacts-file input/contacts.txt`

```bash
The contacts file contains 100 people in it! Lets get searching!

  We are looking for contacts who have a job related to "engineer":
  joe70@yahoo.com is a Network engineer
  torresjames@white.info is a Electrical engineer
  gharris@villarreal-snow.com is a Water engineer
  williamsondavid@lopez.com is a Automotive engineer
  ronald83@yahoo.com is a Maintenance engineer
  zmarshall@yahoo.com is a Control and instrumentation engineer
  christopher35@yahoo.com is a Civil engineer, consulting
  edwardsjacob@gmail.com is a Chemical engineer

Wow, we found some contacts! Email them to learn about your job!
```

- `poetry run contactsearcher --job-description "neer" --contacts-file input/contacts.txt`

```bash
The contacts file contains 100 people in it! Lets get searching!

  We are looking for contacts who have a job related to "neer":
  joe70@yahoo.com is a Network engineer
  torresjames@white.info is a Electrical engineer
  grahamjoel@castillo-gilbert.net is a Engineer, technical sales
  gsutton@miller.com is a Engineer, maintenance
  gharris@villarreal-snow.com is a Water engineer
  williamsondavid@lopez.com is a Automotive engineer
  ronald83@yahoo.com is a Maintenance engineer
  zmarshall@yahoo.com is a Control and instrumentation engineer
  christopher35@yahoo.com is a Civil engineer, consulting
  jacquelinedavid@hotmail.com is a Engineer, electronics
  espinozadaryl@hill-maddox.com is a Engineering geologist
  edwardsjacob@gmail.com is a Chemical engineer

Wow, we found some contacts! Email them to learn about your job!
```

## Source Code and Configuration Files

### Describe in detail how your provided source code works

#### The source code statement that makes the `search` module available to `main`

```python
from contactsearcher import search
```

This imports search from contact searcher. This imports search.
Make sure that you delete all of the markers and the written prompts
from this document. You should also ensure that the document does not have any
mistakes in spelling, grammar, or the syntax of Markdown. Ultimately, the final
version of your reflection should be a polished document that is suitable for
publication on your web site.


#### The source code statement that extracts the current job description for a contact

```python
def contactsearcher(
    job_description: str = typer.Option(..., prompt=True),
    contacts_file: Optional[Path] = typer.Option(None),
) -> None:
```

Make sure that you delete all of the markers and the written prompts
from this document. You should also ensure that the document does not have any
mistakes in spelling, grammar, or the syntax of Markdown. Ultimately, the final
version of your reflection should be a polished document that is suitable for
publication on your web site.

#### Invocation of the function called `search_for_email_given_job`

```python
find = search.search_for_email_given_job(job_description, contacts_file)
```

Make sure that you delete all of the markers and the written prompts
from this document. You should also ensure that the document does not have any
mistakes in spelling, grammar, or the syntax of Markdown. Ultimately, the final
version of your reflection should be a polished document that is suitable for
publication on your web site.

#### Test case for the function called `search_for_email_given_job`

```python
def test_find_one_matching_result():
    contacts_database = """kylebarnes@hotmail.com,Records manager
joe70@yahoo.com,Network engineer
torresjames@white.info,Electrical engineer
shawkins@watson.com,Science writer"""
    contacts_list = search.search_for_email_given_job("writer", contacts_database)
    assert len(contacts_list) == 1
```

Make sure that you delete all of the markers and the written prompts
from this document. You should also ensure that the document does not have any
mistakes in spelling, grammar, or the syntax of Markdown. Ultimately, the final
version of your reflection should be a polished document that is suitable for
publication on your web site.

#### Execute trace of the `contactsearcher` program

```python
def search_for_email_given_job(job_description: str, contacts: str) -> List[List[str]]:
```

TODO: Your discussion should start with the invocation of the `contactsearcher`
function in the `main` module, explain all of the subsequent function calls in
the correct order, and then show how the program's control returns to the
`contactsearcher` function in the `main` module.

- `poetry run contactsearcher --job-description "engineer" --contacts-file input/contacts.txt`

Make sure that you delete all of the markers and the written prompts
from this document. You should also ensure that the document does not have any
mistakes in spelling, grammar, or the syntax of Markdown. Ultimately, the final
version of your reflection should be a polished document that is suitable for
publication on your web site.

## Professional Assessment

### So far this semester, what is one area in which you have struggled? How did you overcome this challenge?

I have struggled completing all of the reflections. Between this class and compsci
101, there is a lot of writing to do on top of how long the reflections are to
begin with.

### Based on your experiences with this project, what is one way in which you want to improve?

I wish to be more efficent. Sometimes I feel like I spend an eternity on the
same issue.
