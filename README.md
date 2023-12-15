# gitactㅁㅁㅇ
ㅇㅇㅇㅇ
      <jacoco:coverage destfile="build/jacoco.exec">
         <junit fork="true" forkmode="once">
            <classpath>
               <pathelement path="build/classes" />
            </classpath>
            <formatter type="plain" usefile="false" />
            <batchtest>
               <fileset dir="src">
                  <include name="**/*Test.java" />
               </fileset>
            </batchtest>
         </junit>
      </jacoco:coverage>
   </target>

   <!-- 코드 커버리지 리포트 생성 태스크 -->
   <target name="report">
      <jacoco:report>
         <executiondata>
            <file file="build/jacoco.exec" />
         </executiondata>
         <structure name="YourProject">
            <classfiles>
               <fileset dir="build/classes" />
            </classfiles>
            <sourcefiles encoding="UTF-8">
               <fileset dir="src" />
            </sourcefiles>
         </structure>
         <html destdir="build/jacoco-report" />
      </jacoco:report>
   </target>
