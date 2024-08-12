srcdir=..

FILES = \
	'post/to.html' \
	'Evidence/Discovery of Defendant/Discovery Answers v1.pdf' \
	'2015-08-28 - Statement of Claim/T-1450-15 Statement of Claim.pdf' \
	'2015-09-29 - Defendant Statement of Defence/T-1450-15 STATEMENT OF DEFENCE.pdf' \
	'2015-11-06 - Affidavit of Documents - Defence/T-1450-15_0.pdf' \
	'2015-11-06 - Affidavit of Documents - Defence/T-1450-15_14 - Nov 19 2014 Kendall receives LePage ruling.pdf' \
	'2015-11-06 - Affidavit of Documents - Defence/T-1450-15_16 - Dec 11 2014 letter from Kendall.pdf' \
	'2016-08-30 - Defendant Motion to Dismiss/Aug 30 2016 - Defendant Notice of Motion to dismiss 16945818.pdf' \
	'2017-02-28 - Motion for Summary Judgement by defendant/T-1450-15 - HociungSummaryJudgementMotion.pdf' \
	'2017-02-28 - Motion for Summary Judgement by defendant/T-1450-15 Response to Summary Judgement Motion.pdf' \
	'2017-02-28 - Motion for Summary Judgement by defendant/PetersonDiscovery.pdf' \
	'2018-03-16 - Summary + Amendment Judgments/T-1450-15_20180315_JR_E_O_OTT_20180319092218_GL2_2018_FC_298.pdf' \
	'2018-04-05 - Appeal Notices/A-101-18_Notice of Appeal.pdf' \
	'2018-04-05 - Appeal Notices/A-102-18_Notice of Appeal.pdf' \
	'2018-05-08 - Appeal summary/A-102-18 - Appeal Book.pdf' \
	'2018-05-08 - Appeal summary/A-102-18-Appeal-Book-Aug12-2018.pdf' \
	'2019-02-28 - Respondent Memo of Fact and Law/File_A-101-18_20190226.PDF' \
	'2019-06-07 - Representations to Court/A-101-18 & A-102-18.pdf' \
	'2019-06-07 - Representations to Court/HociungA-101-18&A-102-18LetterJune10.pdf' \
	'2019-08-07 - Appeals Judgments/A-101-18_20190807_J_E_O_OTT_20190807121032_GTR_WBB_RVO.pdf' \
	'2019-08-07 - Appeals Judgments/A-101-18_20190807_R_E_O_OTT_20190807121751_GTR_WBB_RVO_2019_FCA_215.pdf' \
	'2019-08-07 - Appeals Judgments/A-102-18_20190807_R_E_O_OTT_20190807115620_GTR_WBB_RVO_2019_FCA_214-anotated.pdf' \
	'2019-08-07 - Appeals Judgments/A-102-18_20190807_J_E_O_OTT_20190807111959_GTR_WBB_RVO.pdf' \
	'2020-06-16 - Recusal Decision/T-1450-15.pdf' \
	'Evidence/Discovery of Defendant/Discovery Answers v1.pdf' \
	'Evidence/Discovery of Defendant/Discovery Answers v1-CBSA Precious Metals Memo.pdf' \
	'Evidence/FINTRAC inquiry re gold/FINTRAC Policy Interpretation Re gold coins inquiry.pdf' \
	'Evidence/CCRA Contributions/AMPS first mention EY Sep 22 1997 - question mark.pdf' \
	'Evidence/CCRA Contributions/GST MEmo 7.5 Electronic Filing and Remitting - April 1997 - compliance record.pdf' \
	'Evidence/CCRA Contributions/Administrative/P-134 - Requirement for returns by non-resident performers staging events in Canada - November 30, 1993.pdf' \
	'Evidence/CCRA Contributions/Administrative/P-169 - Meaning of in-respect-of - January 25, 1995.pdf' \
	'Evidence/CCRA Contributions/Administrative/P-200 - Place of supply of intangible personal property and real property - by Gleeson - January 1, 1996.pdf' \
	'Evidence/CCRA Contributions/Administrative/P-212 - Entitlement of visiting forces members - by Gleeson Sep 12, 1997.pdf' \
	'Evidence/Exhibit K - Customs-Enforcement-Manual-2-of-3.pdf' \
	'Evidence/Exhibit K - Customs-Enforcement-Manual-3-of-3.pdf' \
	'Evidence/Khaled Nawaya case/Khaled Nawaya BCSC-179965.pdf'

# Variables
LINKDIR := out

SHELL=/bin/bash

# Rule to replace spaces with underscores in the paths
all:
	@mkdir -p $(LINKDIR)
	@set -o errexit ; \
	set -x ; \
	for file in $(FILES); do \
		echo "Working on $$file"; \
		link_file=$${file// /_}; \
		echo make "___________ $(LINKDIR)/$$link_file" ; \
		$(MAKE) "$(LINKDIR)/$$link_file" SRC="$(srcdir)/$$file"; \
	done

checkout:
	@set -o errexit ; \
	for file in $(FILES); do \
		echo "Working on $$file"; \
		git checkout master -- "$(srcdir)/$$file"; \
	done

# Replace spaces with underscores in the filenames and create hardlinks
$(LINKDIR)/%:
	@mkdir -p "$(dir $@)"
	@ln "$(SRC)" "$@"


