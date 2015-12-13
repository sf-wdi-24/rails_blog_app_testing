# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> Rails Blog App Continued: Testing

**Objective:** Use Rails to build a full-stack blog application. You will be building this app over the course of three evenings.

**Your objective for this evening is to add controller specs for one resource in your blog app.**

## Getting Started

1. Make a new branch in your <a href="https://github.com/sf-wdi-24/rails_blog_app" target="_blank">rails_blog_app</a> called `testing`.
2. Implement the minimum requirements below.

## Minimum Requirements

* Controller specs for ONE resource in your application. This can either be `users`, `posts`, or `comments` (if your blog has comments).

* Use the <a href="https://github.com/thoughtbot/factory_girl_rails" target="_blank">factory_girl_rails</a> and <a href="https://github.com/ffaker/ffaker" target="_blank">ffaker</a> gems to set up a factory for the resource you choose to test.

* Use RSpec to write specs for all of your resource's controller methods, i.e. `index`, `new`, `create`, `show`, `edit`, `update`, `destroy`.

* Start by writing out in English what each controller method should do in the "success" case. Example assertions for `posts#index`:
  * It should assign the instance variable `@posts` to equal all posts.
  * It should render the `:index` view.

  Those assertions are your tests!

  **Note:** If you're testing routes that require authorization, remember to create and log in a user before running the test. You can use a `user` factory and log in the user by setting `session[:user_id]` directly in the test.

* Read the getting started guide for the <a href="https://github.com/colszowka/simplecov" target="_blank">simplecov</a> gem. Set up simplecov in your app, and see what percentage of test coverage you have!

**If you get stuck at any point or need extra guidance, feel free to look at the <a href="https://github.com/sf-wdi-24/rails_blog_app/tree/solution_testing" target="_blank">solution_testing branch</a> or follow along with the <a href="https://www.railstutorial.org/book" target="_blank">*Ruby on Rails Tutorial* by Michael Hartl</a>.**

## Bonus

* Think about any "error" cases you're currently handling in your controller methods:
  * What happens if model validations fail?
  * Does a user need to be logged in to perform this action? What happens if they're not logged in?

  Write tests for as many "error" cases as you can think of. Example assertions for `posts#create` when validations fail:
    * It should display a flash message with errors.
    * It should redirect to `new_post_path`.

* The best way to get comfortable with testing is by repetition. Don't stop at just one resource. Write specs (success and error cases) for another resource in your app as well!

## Submission

* As you make code changes, frequently commit and push to GitHub.
* Once you've finished the assignment and pushed your work to GitHub, make a pull request from **your `testing` branch** to the original repo.
