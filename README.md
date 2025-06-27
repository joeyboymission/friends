# Rails Friends Application 👥

A Ruby on Rails application built for learning and practicing core Rails concepts. This project demonstrates CRUD operations, scaffolding, database migrations, and modern Rails development practices.

## 🎯 Learning Objectives

This application serves as a hands-on practice project to master:

- **Rails Fundamentals**: MVC architecture, routing, controllers, models, views
- **Database Management**: Migrations, schema design, Active Record
- **Scaffolding**: Rapid prototyping with Rails generators
- **ERB Templates**: Embedded Ruby and view helpers
- **Partials**: Reusable view components
- **Rails Conventions**: Naming, file structure, best practices
- **Version Control**: Git integration with Rails development

## 🚀 Technology Stack

- **Ruby on Rails**: 8.0.2 (Latest version)
- **Database**: SQLite3
- **Frontend**: Turbo + Stimulus (Hotwire)
- **Asset Pipeline**: Propshaft + Importmap
- **Background Jobs**: Solid Queue
- **Caching**: Solid Cache
- **Real-time**: Solid Cable
- **Testing**: Capybara + Selenium
- **Version Manager**: mise

## 📋 Current Implementation Status

### ✅ **Completed Features**
- [x] Rails 8.0.2 application setup with modern stack
- [x] Friend model with attributes (first_name, last_name, email, phone, twitter)
- [x] Complete CRUD operations via scaffold generator
- [x] Database migration and schema setup
- [x] RESTful routing configuration
- [x] Application layout with navigation partial
- [x] ERB templates and Rails helpers implementation
- [x] Git version control setup
- [x] Development environment configuration

### 🎯 **Learning Areas Covered**
- [x] Rails naming conventions (singular models, plural controllers)
- [x] Migration vs Schema understanding
- [x] ERB syntax and link_to helpers
- [x] Partial rendering and reusable components
- [x] Rails routing and path helpers
- [x] Scaffold generator and file structure

### 🔄 **Next Learning Steps**
- [ ] Custom validation implementation
- [ ] Form customization and error handling
- [ ] CSS styling and UI improvements
- [ ] Search and filtering functionality
- [ ] Model relationships (has_many, belongs_to)
- [ ] Authentication system
- [ ] Testing implementation
- [ ] Deployment preparation

## 🛠️ Setup Instructions

### Prerequisites
```bash
# Ensure you have Ruby and Rails installed
ruby --version   # Should be 3.x+
rails --version  # Should be 8.0.2
```

### Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/joeyboymission/friends.git
   cd friends
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Setup database**
   ```bash
   rails db:create
   rails db:migrate
   rails db:seed    # Optional: Add sample data
   ```

4. **Start the server**
   ```bash
   rails server
   ```

5. **Visit the application**
   ```
   http://localhost:3000
   ```

## 📁 Project Structure

```
friends/
├── app/
│   ├── controllers/
│   │   ├── application_controller.rb
│   │   └── friends_controller.rb        # CRUD operations
│   ├── models/
│   │   ├── application_record.rb
│   │   └── friend.rb                    # Friend model
│   └── views/
│       ├── layouts/
│       │   └── application.html.erb     # Main layout
│       ├── home/
│       │   └── _header.html.erb         # Navigation partial
│       └── friends/                     # CRUD views
│           ├── index.html.erb
│           ├── show.html.erb
│           ├── new.html.erb
│           ├── edit.html.erb
│           └── _form.html.erb
├── config/
│   ├── routes.rb                        # Application routes
│   └── database.yml                     # Database configuration
├── db/
│   ├── migrate/
│   │   └── 20250626062754_create_friends.rb  # Migration file
│   └── schema.rb                        # Current database structure
└── Gemfile                             # Dependencies
```

## 🎓 Rails Concepts Demonstrated

### 1. **MVC Architecture**
- **Models**: `Friend` model with Active Record
- **Views**: ERB templates with partials
- **Controllers**: `FriendsController` with RESTful actions

### 2. **Database Management**
```ruby
# Migration (Instructions for DB changes)
class CreateFriends < ActiveRecord::Migration[8.0]
  def change
    create_table :friends do |t|
      t.string :first_name
      t.string :last_name
      t.string :email
      t.string :phone
      t.string :twitter
      t.timestamps
    end
  end
end
```

### 3. **ERB and Helpers**
```erb
<!-- Rails helper for generating links -->
<%= link_to "Friends App", root_path, class: "navbar-brand text-white" %>

<!-- Partial rendering -->
<%= render "home/header" %>
```

### 4. **RESTful Routes**
```ruby
# Generated routes for Friend resource
resources :friends
# Creates: index, show, new, create, edit, update, destroy
```

## 🔍 Key Learning Commands

```bash
# Generate scaffold (creates model, controller, views, migration)
rails generate scaffold friend first_name last_name email phone twitter

# Database operations
rails db:create          # Create database
rails db:migrate         # Run pending migrations
rails db:rollback        # Undo last migration
rails db:reset          # Drop, create, and migrate

# Development server
rails server             # Start application server
rails console           # Interactive Rails console

# Code quality
rails test              # Run test suite
rubocop                 # Code style checker
brakeman               # Security scanner
```

## 🎯 Learning Reference

This project follows the tutorial concepts from:
- **YouTube Reference**: [Ruby on Rails Tutorial](https://youtu.be/fmyvWz5TUWg?si=ygOK6wG2uGHPufG_)
- **Rails Guides**: https://guides.rubyonrails.org/
- **Rails API**: https://api.rubyonrails.org/

## 📝 Notes for Practice

### Rails Naming Conventions
- **Models**: Singular (`Friend`)
- **Controllers**: Plural (`FriendsController`)
- **Tables**: Plural (`friends`)
- **Files**: snake_case (`friends_controller.rb`)

### Migration vs Schema
- **Migration**: Step-by-step instructions for database changes
- **Schema**: Current snapshot of entire database structure
- **Timestamp**: YYYYMMDDHHMMSS format for migration ordering

### ERB Syntax
- `<%= %>`: Execute Ruby code AND output result
- `<% %>`: Execute Ruby code WITHOUT output (logic only)

## 🤝 Contributing

This is a personal learning project. Feel free to fork and experiment with your own Rails concepts!

## 📄 License

This project is for educational purposes only.

---

**Happy Rails Learning! 🚀**

*Built with ❤️ for mastering Ruby on Rails*
