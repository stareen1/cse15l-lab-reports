# Week 5 Lab Report 
## Researching Commands

**Grep Options: Searches to find files with the given string and prints the matching lines**

*-c count of matching lines*
```
[cs15lfa22ml@ieng6-201]:skill-demo1:134$ grep -c "purple" technical/*/*.txt
technical/plos/pmed.0020249.txt:0
technical/plos/pmed.0020257.txt:0
technical/plos/pmed.0020258.txt:0
technical/plos/pmed.0020268.txt:0
technical/plos/pmed.0020272.txt:0
technical/plos/pmed.0020273.txt:0
technical/plos/pmed.0020274.txt:0
technical/plos/pmed.0020275.txt:0
technical/plos/pmed.0020278.txt:0
technical/plos/pmed.0020281.txt:0
```
This command printed out the file paths with a number indicating the counts of the number of lines that matched the given string in the command. This is useful when trying to find out how many matching lines there are without actually seeing the lines. 

```
[cs15lfa22ml@ieng6-201]:skill-demo1:134$ grep -c "google" technical/plos/*.txt
technical/plos/journal.pbio.0020001.txt:0
technical/plos/journal.pbio.0020010.txt:0
technical/plos/journal.pbio.0020012.txt:0
technical/plos/journal.pbio.0020013.txt:0
technical/plos/journal.pbio.0020019.txt:0
technical/plos/journal.pbio.0020028.txt:0
technical/plos/journal.pbio.0020035.txt:0
technical/plos/journal.pbio.0020040.txt:0
technical/plos/journal.pbio.0020042.txt:0
technical/plos/journal.pbio.0020043.txt:0
```
This command can be used on specific directories within the main directory as well. 

```
[cs15lfa22ml@ieng6-201]:skill-demo1:135$ grep -c "police" technical/911report/chapter-13*.txt
technical/911report/chapter-13.1.txt:0
technical/911report/chapter-13.2.txt:0
technical/911report/chapter-13.3.txt:3
technical/911report/chapter-13.4.txt:4
technical/911report/chapter-13.5.txt:9
```
This command can also be used on specific names in texts.

*-h shows matching lines without file paths*
```
[cs15lfa22ml@ieng6-201]:skill-demo1:136$ grep -h "police" technical/911report/chapter-13*.txt
                line workers, but not police or the Department of Corrections, from transmitting
            47. On the relationship between the FBI and state and local police forces, see
                screener. The terminal was evacuated, and police found miscellaneous gun parts,
                coincided with a police station bombing in Zagreb where the timing device of the
                other than the CIA. According to Lance, the Philippine police officer, who after
                police custody in Qatar. See CIA briefing by CTC specialists (June 22, 2004); Walter
                Hamburg police, and the UAE official's search, see German BKA report, investigative
                recorded calls to the Port Authority police desk from people in the towers on
                from police that morning.
                special approval by senior U.S. government officials. On September 13, Tampa police
                the airport so they could get on a plane to Lexington. Tampa police arranged for two
                Saudi nationals debarked from the plane and were met by local police. Their private
                security guards were paid, and the police then escorted the three Saudi passengers
                to Lexington by a local police officer in Lexington who did not have firsthand
                White House to kill the president. The man was shot by police and then killed
            8. For Pakistan's unpoliced areas, see Tasneem Noorani interview (Oct. 27, 2003)
```
This command prints out the lines that have the matching string in the files. This is very useful is you don't want all the extra paths that distract from the text.

```
[cs15lfa22ml@ieng6-201]:skill-demo1:140$ grep -h "police station" technical/911report/chapter-13*.txt
                coincided with a police station bombing in Zagreb where the timing device of the
```
This command can also be used with multiple words in a string for more detailed searches.

```
[cs15lfa22ml@ieng6-201]:skill-demo1:142$ grep -h "purple" technical/*/*.txt
            the lower, purple-colored panel of the Selection Frame
          cells to produce a purple formazan product. Schweitzer et
          tetrazolium dye forming a purple color. Other wells
          scoring purple reactions in individual wells as a
          diagram highlights two groups of genes (purple stripes)
          presence of purple NBT precipitate using bright field
        red) and 386-417 (indicated in purple). The orientation of
          or less effort and time than required for bR (purple
          purple membrane. However, there is one major difference:
          malnutrition [ 52 54 65 ] . The purple-red juice from the
          plates were allowed to air dry. The purple formazan
          bromide] to purple formazan crystals by metabolically
          purple color was visible (up to 6.5 h). The reaction was
          present in the epithelial cells where the purple label
          only the neutral red staining (Fig. 3B). The purple label
        reaction center (PRC-H) from purple proteobacteria such as
        The purple bacterial photosynthetic reaction center
          the orthologs of the PRC-H proteins from other purple
          purple bacteria [ 14], whereas RimM is a protein that
          purple bacterial PRC-H lies on the cytosolic face of the
          version. In addition to the purple bacteria, such
          by analogy with their purple bacterial counterparts. One
          PRC-barrel through lateral transfer from the purple
        bowl-shaped flowers of different colours (such as yellow, white, and purple, e.g., in the
        humans, mixing violet with red light will produce purple, a sensation that has no
          bromocresol purple method. Fibrinogen was measured using a quantitative assay of clotting
```
This command can also be used for wider searches by searching through multiple directories. 

*-v prints out all the lines that do not match the string*
```
[cs15lfa22ml@ieng6-201]:skill-demo1:146$ grep -v "police" technical/911report/chapter-13.5*.txt
            19. This change should eliminate the need in the Senate for the current procedure of
                sequential referral of the annual authorization bill for the national foreign
                intelligence program. In that process, the Senate Armed Services Committee reviews
                the bill passed by the Senate Select Committee on Intelligence before the bill is
                brought before the full Senate for consideration.
            20. This recommendation, and measures to assist the Bureau in developing its
                intelligence cadre, are included in the report accompanying the Commerce, Justice
                and State Appropriations Act for Fiscal Year 2005, passed by the House of
                Representatives on July 7, 2004. H.R. Rep. No. 108-576, 108th Cong., 2d sess.
                (2004), p. 22.
            21. Letter from Ridge and others to Collins and Levin, Apr. 13, 2004.
            22. For the directorate's current capability, see Patrick Hughes interview (Apr. 2,
                2004).
```
This command printed out all the lines in the specified files that did not have the string "police" in them. This can be useful when you are trying to format a file for example and want to find lines that may not match a pattern in order to fix them. 

```
[cs15lfa22ml@ieng6-201]:skill-demo1:147$ grep -v "biology" technical/biomed/*.txt
technical/biomed/1471-2407-2-8.txt:          avidin-biotin-peroxidase complex method was used for the
technical/biomed/1471-2407-2-8.txt:          immunostaining of p53, iNOS and VEGF. In brief, after
technical/biomed/1471-2407-2-8.txt:          dewaxing, inactivating endogenous peroxidase activity and
technical/biomed/1471-2407-2-8.txt:          blocking cross-reactivity with normal serum (Vectastain
technical/biomed/1471-2407-2-8.txt:          Elite Kit; Vector, Burlingame, CA), the sections were
technical/biomed/1471-2407-2-8.txt:          incubated overnight at 4□ with a diluted solution of the
technical/biomed/1471-2407-2-8.txt:          primary antibodies (1:1000 for p53, 1:200 for iNOS and
technical/biomed/1471-2407-2-8.txt:          1:100 for VEGF). Location of the primary antibodies was
technical/biomed/1471-2407-2-8.txt:          achieved by subsequent application of a biotinylated
technical/biomed/1471-2407-2-8.txt:          anti-primary antibody, an avidin-biotin complex
technical/biomed/1471-2407-2-8.txt:          conjugated to horseradish peroxidase, and
technical/biomed/1471-2407-2-8.txt:          diaminobenzidine (Vectastain Elite Kit, Vector,^C
```
This command is probably most useful for a small number of files if not many lines have the specified string in them. This command took almost 30 seconds to run through all the lines in this directory!

```
[cs15lfa22ml@ieng6-201]:skill-demo1:147$ grep -v "biology" technical/biomed/1468-6708-3-1.txt

        Introduction
        Older adults are frequently counseled to lose weight,
        even though there is little evidence that overweight is
        associated with increased mortality in those over age 65.
        Six large controlled population-based studies of
        non-smoking older adults have investigated the association
        between body mass index (BMI) and mortality, controlling
        for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
        excess risk for persons with very low BMI, but that persons
        with moderately high BMI had little or no extra risk except
        in certain small subsets. A review of 13 studies of older
        adults drew similar conclusions [ 7 ] .
```
This command can also be used on one specific file. However, there was still a lot of output printed so this command may be more useful in smaller files or in files where most of the lines will have the specified string. 


