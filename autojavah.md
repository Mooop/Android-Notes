#autojavah.sh
<div><div>export ProjectPath=$(cd "../$(dirname "$1")"; pwd)</div><div>export TargetClassName="package path + Activity Name" #!example com.example.mop.testndk.MainActivity</div><div><br></div><div>export SourceFile="${ProjectPath}/SourceFile path" #! example TestNDK/app/src/main/java</div><div>export TargetPath="${ProjectPath}/TargetPath" #! TestNDK/app/src/main/jni</div><div><br></div><div>cd "${SourceFile}"</div><div>javah -d ${TargetPath} -classpath "${SourceFile}" "${TargetClassName}"</div><div>echo -d ${TargetPath} -classpath "${SourceFile}" "${TargetClassName}"</div></div>

you can put it in your project root directory(create a new file and name end with .sh).
