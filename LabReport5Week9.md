# Lab Report 5 - Week 9
## Sarah Tareen

**Grade.sh**
```
rm -rf student-submission
git clone $1 student-submission
echo "Finished cloning"

cd student-submission
GRADE=0
if [[ ! -f ListExamples.java ]]
then 
    echo "ListExamples.java not found"
    echo "Grade out of 3: "$GRADE
    exit 1
fi
GRADE=1

cd ..
cp TestListExamples.java student-submission/
cp -r lib student-submission/
cd student-submission/

javac -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar *.java
if [[ $? -ne 0 ]]
then
  echo "ListExamples.java does not compile"
  echo "Grade out of 3: "$GRADE
  exit 1
fi
GRADE2

java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples

if [[ $? -ne 0 ]]
then
  echo "Failed tests"
  echo "Grade out of 3: "$GRADE
else
  echo "Passed all tests"
  echo "Grade out of 3: 3"
fi
```
![Image](Screenshot(15).png)



