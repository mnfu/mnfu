```java
import java.util.ArrayList;

class Main {
    public static void main(String[] args) {
        AboutMe aboutMe = new AboutMe("Rob");

        aboutMe.setDescription("I use github to browse projects I find interesting, and to organize my personal ones!");
        aboutMe.addAlias("mnfu");
        aboutMe.addAlias("Partayyy");

        System.out.println("Name: " + aboutMe.getName() + "\nAliases: " + aboutMe.getAliases() + "\nDescription: " + aboutMe.getDescription());
    }
}

class AboutMe {
    private String name = "";
    private String description = "";
    private String allAliases = "";
    private ArrayList<String> aliases = new ArrayList<>();

    public AboutMe() {}

    public AboutMe(String newName) {
        name = newName;
    }

    public void addAlias(String newAlias) {
        aliases.add(newAlias);
    }

    public void setDescription(String desc) {
        description = desc;
    }

    public String getName() {
        return name;
    }

    public String getAliases() {
        for (int i = 0; i < aliases.size(); i++) {
            allAliases += aliases.get(i);
            if(i + 1 < aliases.size()) {
                allAliases += ", ";
            }
        }
        return allAliases;
    }

    public String getDescription() {
        return description;
    }
}
```
