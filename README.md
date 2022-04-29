### Hi there 👋

This is me:

```go
package main

import "fmt"

func main() {
	me := struct {
		Name         string
		Surname      string
		Country      string
		City         string
		Job          string
		Technologies []string
		Databases    []string
		Frameworks   []string
		Interests    []string
		Hobbies      []string
		Contacts     []string
	}{
		Name:         "Daniel M.",
		Surname:      "Spiridione",
		Country:      "Argentina",
		City:         "Ciudad Autónoma de Buenos Aires",
		Job:          "Software Developer",
		Technologies: []string{"PHP", "Go", "Javascript", "Kotlin", "HTML5", "CSS3"},
		Databases:    []string{"MySQL", "MariaDB", "PostgreSQL", "Redis", "MongoDB"},
		Frameworks:   []string{"Symfony", "React", "Fiber"},
		Interests:    []string{"Clean Architecture", "Domain Driven Design", "Microservices", "RESTful", "gRPC", "CQRS"},
		Hobbies:      []string{"Fishing", "Welding", "Kayaking", "Trekking", "Beer"},
		Contacts:     []string{"daniel.spiridione@gmail.com", "https://ar.linkedin.com/in/daniel-mart%C3%ADn-spiridione-46695528", "https://github.com/danielspk"},
	}

	fmt.Printf("😃 Hello, my name is `%s %s`\n", me.Name, me.Surname)
	fmt.Printf("🌏 I live in %s - %s\n", me.City, me.Country)
	fmt.Printf("💻 I work as a %s\n", me.Job)
	fmt.Println("💪 These are my skills and interests:")
	for _, s := range append(append(append(append(me.Technologies, me.Databases...), me.Frameworks...), me.Interests...), []string{"..."}...) {
		fmt.Printf("   - %s\n", s)
	}
	fmt.Println("🚀 When I'm not working I like:")
	for _, h := range me.Hobbies {
		fmt.Printf("   - %s\n", h)
	}
	fmt.Println("📬 You can contact me at:")
	for _, c := range me.Contacts {
		fmt.Printf("   - %s\n", c)
	}
}
```
