# Android-Notes
It marks some android development notes. :-D

#autojavah.sh
export ProjectPath=$(cd "../$(dirname "$1")"; pwd)
export TargetClassName="package path + Activity Name" #!example com.example.mop.testndk.MainActivity

export SourceFile="${ProjectPath}/SourceFile path" #! example TestNDK/app/src/main/java
export TargetPath="${ProjectPath}/TargetPath" #! TestNDK/app/src/main/jni

cd "${SourceFile}"
javah -d ${TargetPath} -classpath "${SourceFile}" "${TargetClassName}"
echo -d ${TargetPath} -classpath "${SourceFile}" "${TargetClassName}"
