The two directories i and ii contain (respectively) the chapters
from the courses, each one in its separate .tex file. They are
included via the \include command in the main source file, that is
analisi-matematica.tex in the root directory of the project.

Every figure is created with pgfplots and externalized, and its
code written in a dedicated .tex file in the grafici directory,
which is \input in the document when needed.

