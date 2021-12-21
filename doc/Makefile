# Minimal makefile for Sphinx documentation
MKFILE_DIR:=$(dir $(abspath $(lastword $(MAKEFILE_LIST))))

# You can set these variables from the command line, and also
# from the environment for the first two.
SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = source
BUILDDIR      = build

TARGETS += html
TARGETS += dirhtml
TARGETS += singlehtml
TARGETS += pickle
TARGETS += json
TARGETS += htmlhelp
TARGETS += qthelp
TARGETS += devhelp
TARGETS += epub
TARGETS += latex
TARGETS += latexpdf
TARGETS += latexpdfja
TARGETS += text
TARGETS += man
TARGETS += texinfo
TARGETS += info
TARGETS += gettext
TARGETS += changes
TARGETS += xml
TARGETS += pseudoxml
TARGETS += linkcheck
TARGETS += doctest
TARGETS += coverage
TARGETS += clean

# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

$(MKFILE_DIR)/.venv : $(MKFILE_DIR)/requirements.txt
	python3 -m venv $(MKFILE_DIR)/.venv
	$(MKFILE_DIR)/.venv/bin/python3 -m pip install -r $(MKFILE_DIR)/requirements.txt

.PHONY: help

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
$(TARGETS): $(MKFILE_DIR)/.venv
	@cd $(MKFILE_DIR) ; \
		$(MKFILE_DIR)/.venv/bin/$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)



