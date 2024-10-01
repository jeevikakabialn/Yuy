@model AdmissionCollege.Models.StudentRegistration

@{
    ViewBag.Title = "StudentRegistration";
    Layout = null;
}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Student Registration</title>
    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" rel="stylesheet" />
    <style>
        /* Optional additional styling */
        body {
            background-color: #f4f7fc;
        }

        .card-header {
            text-align: center;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container mt-5">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Student Registration</div>
                    <div class="card-body">
                        @using (Html.BeginForm("StudentRegistration", "Login", FormMethod.Post))
                        {
                            @Html.AntiForgeryToken()

                            <div class="form-row">
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.StudentID)
                                    @Html.EditorFor(model => model.StudentID, new { htmlAttributes = new { @class = "form-control", @id = "StudentID", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.StudentID, "", new { @class = "text-danger" })
                                </div>
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.PassWord)
                                    @Html.EditorFor(model => model.PassWord, new { htmlAttributes = new { @class = "form-control", @id = "PassWord", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.PassWord, "", new { @class = "text-danger" })
                                </div>
                            </div>

                            <div class="form-row">
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.FirstName)
                                    @Html.EditorFor(model => model.FirstName, new { htmlAttributes = new { @class = "form-control", @id = "FirstName", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.FirstName, "", new { @class = "text-danger" })
                                </div>
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.LastName)
                                    @Html.EditorFor(model => model.LastName, new { htmlAttributes = new { @class = "form-control", @id = "LastName", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.LastName, "", new { @class = "text-danger" })
                                </div>
                            </div>

                            <div class="form-row">
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.DateOfBirth)
                                    @Html.EditorFor(model => model.DateOfBirth, new { htmlAttributes = new { @class = "form-control", @id = "DateOfBirth", @type = "date", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.DateOfBirth, "", new { @class = "text-danger" })
                                </div>
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.Gender)
                                    @Html.EditorFor(model => model.Gender, new { htmlAttributes = new { @class = "form-control", @id = "Gender", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.Gender, "", new { @class = "text-danger" })
                                </div>
                            </div>

                            <div class="form-row">
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.Email)
                                    @Html.EditorFor(model => model.Email, new { htmlAttributes = new { @class = "form-control", @id = "Email", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.Email, "", new { @class = "text-danger" })
                                </div>
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.PhoneNumber)
                                    @Html.EditorFor(model => model.PhoneNumber, new { htmlAttributes = new { @class = "form-control", @id = "PhoneNumber", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.PhoneNumber, "", new { @class = "text-danger" })
                                </div>
                            </div>

                            <div class="form-row">
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.Address)
                                    @Html.EditorFor(model => model.Address, new { htmlAttributes = new { @class = "form-control", @id = "Address", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.Address, "", new { @class = "text-danger" })
                                </div>
                                <div class="form-group col-md-6">
                                    @Html.LabelFor(model => model.Nationality)
                                    @Html.EditorFor(model => model.Nationality, new { htmlAttributes = new { @class = "form-control", @id = "Nationality", @required = "required" } })
                                    @Html.ValidationMessageFor(model => model.Nationality, "", new { @class = "text-danger" })
                                </div>
                            </div>

                            <button type="submit" class="btn btn-primary btn-block">Next</button>
                        }
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.11.0/umd/popper.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js"></script>
</body>
</html>
