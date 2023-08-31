# Programming Parallel Computers, University of Helsinki CSM14212, 2023–2024

See information on the previous year's course [here](/2022).

## General information

### Schedule

The course is open for the entire academic year 2023–2024, specifically from
1.9.2023 to 31.8.2024. You can complete it on your own schedule and there are
no other deadlines.

For technical reasons, the course is initially marked as ending on 31.12.2023
in SISU, but you can disregard this. If you are unable to enrol on the course
(e.g. because you don't have a study right for the whole duration), that is not
necessary. Make sure to request credits before your study right ends, however.

### Discussion

Join the course Discord channel via
<https://study.cs.helsinki.fi/discord/join/ppc>. This is the primary avenue for
asking for help and other discussion about the course.

### Contact

Antti Laaksonen
([ahslaaks@cs.helsinki.fi](mailto:ahslaaks@cs.helsinki.fi)) is responsible
for the course administration. Roope Salmi
([roope.j.salmi@helsinki.fi](mailto:roope.j.salmi@helsinki.fi)) serves
as a teaching assistant and is responsible for the technical aspect of
the course.

### Content

The course is designed to be completed in six intensive weeks, plus the
prerequisite test. You may wish to complete the course at a slower pace. For
instance, last year the University of Helsinki version of the course stretched
each "week" into two calendar weeks.

Lecture material and recordings of lectures given by Jukka Suomela are available
at <https://ppc.cs.aalto.fi/>.

Exercises are described and submitted at
<https://ppc-exercises.cs.aalto.fi/course/hy2023>.

The coursework is divided into _exercises_ and _tasks_. The tasks within each
exercise focus on the same computational problem, but the intended techniques
to solve them are different in each task.

Tasks are numbered according to the week they are intended to be worked on. It
is not necessary to complete, much less get full points in all of them to
achieve a good grade. However, weeks 1–5 have **mandatory** tasks, each of which
you will need to get *at least one point* in to get course credits.

Some tasks have specific instructions that you should follow. Please read those
and more about the structure of the course [below](#course-structure).

## Participating

Read the instructions at <https://ppc-exercises.cs.aalto.fi/help> carefully.

Some details in the instructions only apply to lecture courses with weekly
deadlines. Specific to this course,

- There is less human feedback. Occasional spot checks may be made to confirm
  that you are following the instructions of each task correctly. Also check
  the [course structure](#course-structure) for additional clarifications to
  the task instructions.
- The option "This submission is ready for grading" is selected for you
  automatically. This means that your submission is visible to course staff and
  subject to manual review. If you do not want this for a specific submission,
  select "Please ignore this submission". Selecting this means you cannot get
  any points from the submission.

There is a feature for testing and iterating on your code remotely, which
you may want to utilize to get more accurate measurements or especially if you
do not have an NVIDIA GPU with CUDA development tools installed.

If, for example, you used this command to test locally:

```
./grading test
```

then you can add the `--remote` flag to run the command remotely instead.

```
./grading test --remote
```

When trying this for the first time, you will be instructed to configure an API
token. Obtain an API token at <https://ppc-exercises.cs.aalto.fi/token>, and
paste it into a configuration file in one of the suggested locations.

Your code and the specified tests are then sent to our grading servers, where
they are run on the same hardware as normal submissions are. The output should
otherwise be the same as when running locally, but it is only shown when the
whole command is completed, so be patient.

Be mindful of other users, as the resources are limited and shared with normal
submissions.

### Completing the course

Grading is described at the end of the course page,
<https://ppc-exercises.cs.aalto.fi/course/hy2023>. The minimum amount of points
for course credits is 48. Additionally, you must have at least one point from
every mandatory task, i.e. CP1, MF2, CP3a, SO4 and CP5.

Once you are satisfied with the points and grade you have achieved, contact
Antti Laaksonen ([ahslaaks@cs.helsinki.fi](mailto:ahslaaks@cs.helsinki.fi)) and
provide the email address associated with your account and your student number
so we can register your credits in SISU. We may still review some of your
submissions at this point, but you will be able to go back and fix the issues
if it affects your grade.

## Course structure

### Week 0

This week consists of the task *Pre0*, the prerequisite test worth one course
point. It is not required, but some knowledge of C++ is assumed as
prerequisite for the course. It is possible to complete the course without
much prior knowledge in C++, but this will be more challenging and require
additional self-study.

### Week 1

Introduction to the course and instruction-level parallelism.

Tasks this week: CP1, MF1

**Mandatory task: CP1**

You are introduced to the exercises CP (correlated pairs), and MF (median
filter). The tasks CP1 and MF1 have you implement baseline CPU solutions to
these exercises, which are then improved upon using various techniques in
further weeks.

### Week 2

Multicore parallelism with OpenMP and vector operations.

Tasks this week: CP2a, CP2b, CP2c, MF2

**Mandatory task: MF2**

**Important:** In tasks CP2abc, it is intended that you only use one technique
in each task, and not e.g. all previous techniques combined. CP2a is about
instruction-level parallelism, CP2b is about multicore parallelism, and CP2c is
about vector operations. The techniques will be combined next week.

### Week 3

Combining vectorization, instruction-level and multicore parallelism. Reusing
data in registers and cache.

Tasks this week: CP3a, CP3b

**Mandatory task: CP3a**

It is intentionally very challenging to get full points from these tasks. You
will need to apply your knowledge and experiment with different approaches.

### Week 4

Introduction to GPU and CUDA programming.

Tasks this week: CP4, IS4, SO4

**Mandatory task: SO4**

**Important:** Remember to check for CUDA errors following the instructions in
<https://ppc.cs.aalto.fi/ch4/v0/>. Read the SO exercise rules
<https://ppc-exercises.cs.aalto.fi/course/hy2023/so> carefully

### Week 5

GPU programming in depth.

Tasks this week: CP5, SO5

**Mandatory task: CP5**

**Important:** In task SO5, you should follow the general idea of quicksort for
multiple levels of recursion, before falling back to a different
single-threaded algorithm.

### Week 6

Assorted algorithmic techniques for designing high performance parallel
programs. Concluding the course.

Tasks this week: IS6a, IS6b, SO6

### Additional tasks

There are also the additional tasks CP9a, IS9a, MF9a and X9a which you may want
to do for further insight and course points.

If you find mistakes or bugs in either the course material or the grading
system and report them on the Discord channel, you can get 1 course point via
task X9a.

**Important:** For CP9a, you must use Strassen's algorithm. Submitting a
solution from another CP task will not be accepted.
