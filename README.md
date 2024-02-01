
## BigShool
-------------------
Link: [Tutorial BigSchool](https://github.com/anvndev/BigSchool_AVN/blob/main/Thay-Anh-noi-dung-giang-day-lap-trinh-web.pdf)
<br>
Visual Studio: https://visualstudio.microsoft.com/
<br>
Tutorial Js Ajax: https://www.w3schools.com/js/js_ajax_intro.asp
<br>
Bootstrap: https://getbootstrap.com/

```````html
@using Microsoft.AspNet.Identity
@model BigSchool.Models.ManageUserViewModel

<p>You're logged in as <strong>@User.Identity.GetUserName()</strong>.</p>

@using (Html.BeginForm("Manage", "Account", FormMethod.Post, new { @class = "form-horizontal", role = "form" }))
{
    @Html.AntiForgeryToken()
    <h4>Change Password Form</h4>
    <hr />
    @Html.ValidationSummary()
    <div class="form-group">
        @Html.LabelFor(m => m.OldPassword, new { @class = "col-md-2 control-label" })
        <div class="col-md-10">
            @Html.PasswordFor(m => m.OldPassword, new { @class = "form-control" })
        </div>
    </div>
    <div class="form-group">
        @Html.LabelFor(m => m.NewPassword, new { @class = "col-md-2 control-label" })
        <div class="col-md-10">
            @Html.PasswordFor(m => m.NewPassword, new { @class = "form-control" })
        </div>
    </div>
    <div class="form-group">
        @Html.LabelFor(m => m.ConfirmPassword, new { @class = "col-md-2 control-label" })
        <div class="col-md-10">
            @Html.PasswordFor(m => m.ConfirmPassword, new { @class = "form-control" })
        </div>
    </div>

    <div class="form-group">
        <div class="col-md-offset-2 col-md-10">
            <input type="submit" value="Change password" class="btn btn-default" />
        </div>
    </div>
}

/@anvndev@/
