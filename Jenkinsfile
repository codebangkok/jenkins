import groovy.json.JsonSlurper
import java.io.*

node {
    stage("Hello") {
        echo "Hello World Build $BUILD_NUMBER"

        String path = "/covers.json"
        def json = new JsonSlurper()
        ArrayList covers = json.parse(new File(path))
        for(cover in covers) {
            println(cover.id + " - " + cover.name)
        }
        
        // def x = 5
        // x += 5
        // println(x)
        // assert x == 10: "x not equal 10"

        // String name = "Joke"
        // int age = 19
        // println name + " age " + age.toString()

        // String[] singers = ["Bob","George"]
        // for (singer in singers) {
        //     println singer
        // }
        // singers.each{x -> println(x)}
    }
}