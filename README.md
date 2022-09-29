# REST_API_template
Django REST API template for default authentication backend.

This is a Django project with a REST API application for user authentication data.

You can integrate the app into your existing Django project to manage/view/extend user data to other apps.

To integrate into your existing Django project:

1. Move the "authentication_API" app folder into your project folder and migrate
2. Add 'rest_framework' to INSTALLED_APPS in your settings.py if previously unused
3. Add REST framework routers and authentication_API views to you main urls.py file (lines 3-8 in urls.py)
4. Add REST API interface to your urlpatterns in urls.py (lines 11-12 in urls.py)
5. Modify first argument in line 11 to your desired REST API interface URL path

To serialize additional/custom Django models to your API

1. Duplicate classes in serializers.py in the "authentication_API" app
2. Rename class names, "model" values, and "fields" values accordingly
3. Duplicate classes in views.py in the "authentication_API" app
4. Change "queryset" values and "serializer_class" values accordingly
5. Duplicate routers in urls.py in your main project folder
6. Change router.register arguments to your desired URL path and viewsets
