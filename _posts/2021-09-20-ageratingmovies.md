# Can we predict the age rating of a movie just from its description?

Here's the table of contents:

1. TOC
{:toc}

## Who can watch which movies?

Movies often portray content and scenes that are unsuitable for younger au-
diences. As many movies are not rated for age appropriateness, it would be
useful to be able to give automated suggestions based on readily available in-
formation. In this thesis, my goal is to predict the suitability of movies for
specific age groups based on the MPA rating system. Furthermore, I try to
predict the specific reasons a movie was rated in such a way through predict-
ing the severity of 5 sensitive topics. 

Unlike prior research, I did not use full
movie scripts, but tested the viability of using only short plot descriptions. I
created a corpus of MPA rated movies with two types of short descriptions
and their severity ratings in the topics ‘Nudity and Sexuality’, ‘Violence and
Gore’, ‘Profanity’, ‘Alcohol and Drug use’, and ‘Frightening content’. An
LSTM model that incorporates genre and runtime information making rating
predictions on one-sentence descriptions outperforms a Naive Bayes classifier
baseline on word counts by almost 15% in terms of macro-averaged F1-score.
Severity predictions of sensitive topics achieved the best results with violence
and frightening content, with up to 8.7% increase over a Naive Bayes baseline.
Alcohol use and nudity were the hardest to predict, but still improved predic-
tion on short descriptions by at least 3%. Joint predictions of the component
severities reduced variance in prediction results. By examining the misclas-
sifications of the model, I identified descriptions that might be misleading to
viewers. The model can therefore also be used for optimizing the process of
writing and evaluating descriptions for film.

## MPA rating system

- G: General Audiences. All ages permitted. May not contain any nudity, sex scenes, drug use or strong words, and only minimal violence is permitted.
- PG: Parental Guidance Suggested. Some Material May Not Be Suitable For Children. May contain some profanity, some depictions of violence or brief nudity. No drug use.
- PG-13: Parents Strongly Cautioned. Some Material May Be Inappropriate For
Children Under 13. May contain longer nudity but usually not sexually oriented, depictions of
violence but not realistic and extreme or persistent, a single use of sexually-derived profanity is allowed but only as an expletive. May include drug use.
- R: Children Under 17 Require Accompanying Parent or Adult Guardian. Contains adult material. May include adult themes, adult activity, hard language, intense or persistent violence, sexually-oriented nudity, drug abuse or other elements.
- NC-17: No One 17 and Under Admitted. Only appropriate for an adult audience. May include graphic depictions of violence, sex, aberrational behavior, drug abuse or any other element that
most parents would consider too strong and therefore off-limits for viewing by their children.

---

<!--## Lists

Here's a list:

- item 1
- item 2

And a numbered list:

1. item 1
1. item 2

## Boxes and stuff

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Images

![](/images/logo.png "fast.ai's logo")

## Code

General preformatted text:

    # Do a thing
    do_thing()

Python code and output:

```python
# Prints '2'
print(1+1)
```

    2

## Tables

| Column 1 | Column 2 |
|-|-|
| A thing | Another thing |

## Footnotes

[^1]: This is the footnote. -->

