srcdir=..

FILES = \
	'Evidence/Discovery of Defendant/Discovery Answers v1.pdf' \
	'2015-08-28 - Statement of Claim/T-1450-15 Statement of Claim.pdf' \
	'2015-11-06 - Affidavit of Documents - Defence/T-1450-15_0.pdf' \
	'2015-11-06 - Affidavit of Documents - Defence/T-1450-15_14 - Nov 19 2014 Kendall receives LePage ruling.pdf' \
	'2017-02-28 - Motion for Summary Judgement by defendant/T-1450-15 Response to Summary Judgement Motion.pdf' \
	'2018-04-05 - Appeal Notices/A-101-18_Notice of Appeal.pdf' \
	'2018-05-08 - Appeal summary/A-102-18 - Appeal Book.pdf' \
	'2018-05-08 - Appeal summary/A-102-18-Appeal-Book-Aug12-2018.pdf' \
	'2020-06-16 - Recusal Decision/T-1450-15.pdf' \
	'Evidence/FINTRAC inquiry re gold/FINTRAC Policy Interpretation Re gold coins inquiry.pdf' \
	'Evidence/CCRA Contributions/AMPS first mention EY Sep 22 1997 - question mark.pdf' \
	'Evidence/CCRA Contributions/GST MEmo 7.5 Electronic Filing and Remitting - April 1997 - compliance record.pdf' \
	'Evidence/CCRA Contributions/P-212 - Entitlement of visiting forces members - by Gleeson Sep 12, 1997.pdf'

# Variables
LINKDIR := out

SHELL=/bin/bash

# Rule to replace spaces with underscores in the paths
all:
	@mkdir -p $(LINKDIR)
	set -x ; \
	for file in $(FILES); do \
		echo "Working on $$file"; \
		link_file=$${file// /_}; \
		echo make "___________ $(LINKDIR)/$$link_file" ; \
		$(MAKE) "$(LINKDIR)/$$link_file" SRC="$(srcdir)/$$file"; \
	done

# Replace spaces with underscores in the filenames and create hardlinks
$(LINKDIR)/%:
	@mkdir -p $(dir $@)
	@ln "$(SRC)" $@


