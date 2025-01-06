# NAME

HTML::D3 - A simple Perl module for generating bar charts using D3.js.

# VERSION

Version 0.02

# SYNOPSIS

    use HTML::D3;

    my $chart = HTML::D3->new(
        width  => 1024,
        height => 768,
        title  => 'Sample Bar Chart'
    );

    my $data = [
        ['Category 1', 10],
        ['Category 2', 20],
        ['Category 3', 30]
    ];

    my $html = $chart->render_bar_chart($data);
    print $html;

    $chart = HTML::D3->new(title => 'Sales Data');

    my $data = [
        ['Product A', 100],
        ['Product B', 150],
        ['Product C', 200]
    ];

    $html = $chart->render_bar_chart($data);
    print $html;

# DESCRIPTION

HTML::D3 is a Perl module that provides functionality to create simple bar charts
using D3.js. The module generates HTML and JavaScript code to render the chart in a web browser.

# METHODS

## new

    my $chart = HTML::D3->new(%args);

Creates a new HTML::D3 object. Accepts the following optional arguments:

- `width` - The width of the chart (default: 800).
- `height` - The height of the chart (default: 600).
- `title` - The title of the chart (default: 'Chart').

## render\_bar\_chart

    my $html = $chart->render_bar_chart($data);

Generates HTML and JavaScript code to render a bar chart. Accepts the following arguments:

- `$data` - An array reference containing data points. Each data point should
be an array reference with two elements: the label (string) and the value (numeric).

Returns a string containing the HTML and JavaScript code for the chart.

# AUTHOR

Nigel Horne <njh@bandsman.co.uk>

# LICENSE

This program is released under the following licence: GPL2
