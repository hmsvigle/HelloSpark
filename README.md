# HelloSpark


#----------------  To print length of each line -------------------
val lines = sc.textFile("/apps/lhome/cbnaesb/SPARK/input.log");
val lineLengths = lines.map(s => s.length)
scala> lineLengths.foreach(println)
58
58
58
58
58
56
212
54
122
122
91
122
50
156
102
65

#----------------  To print total length of the file -------------------
val lines = sc.textFile("/apps/lhome/cbnaesb/SPARK/input.log");
val lineLengths = lines.map(s => s.length)
val totalLength = lineLengths.reduce((a, b) => a + b)
 lineLengths: Int = 1442
