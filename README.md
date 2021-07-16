ffa
class end2
fun tax(sum:Double){
  println(sum*0.15)
}

fun main(args:Array<String>){
    print("welcome to the pharmacy alaaelam alakhdar")
    var branch = readLine()!!.toInt()

    var pname = arrayListOf<String>()
    var ltemp = arrayListOf<Double>()
    var i =1
    while (i !=0 ){
        pname.add(readLine()!!)
        ltemp.add(readLine()!!.toDouble())
      println("اضفط 0 لتوقف")
       i= readLine()!!.toInt()
    }
    for(i in 0..pname.size -1)
        for( j in 0..pname.size -1){
            if(ltemp[i] > ltemp[j]){
                var i1 = pname[i]
                var i2 = ltemp[i]

                pname[i] = pname[j]
                ltemp[i] = ltemp[j]

                pname[j] =  i1
                ltemp[j] = i2


            }



        }




            for(i in 0..pname.size -1){
        println(pname[i] + "\t" + ltemp[i])

    }
println(ltemp.sum())

    var sum = ltemp.sum()
    when(branch) {
        1 -> {
            if (sum >= 100)
                println( sum -(sum * 0.10))
        }
        2 -> {
              println(sum)
        }
        3 -> {
            if (sum >= 500)
                println( sum -50)

        }


    }
tax(sum)


}
