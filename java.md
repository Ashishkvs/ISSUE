#DEVTOOLS Configurations
=================
Run using command
add below config in build.gradle
                     ----------------
configurations {
	dev
}
bootRun {
	systemProperties = System.properties
	classpath = sourceSets.main.runtimeClasspath + configurations.dev
}
