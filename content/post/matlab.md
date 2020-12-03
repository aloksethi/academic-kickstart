---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Matlab Plots"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2019-11-01T14:33:41+02:00
lastmod: 2019-11-01T14:33:41+02:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
tags: ["Matlab"]
---
Different color names, marker styles and line styles 
```
% color names and markers
color_name = {'red','green', 'blue', 'black', 'magenta', 'cyan', 'yellow'};
line_style = {':','--','-'};
marker_style = {'o','v','^','s','d','p'};
```
Clearing a figure
```
fig_handle = figure(fig_num);
clf(fig_num); %clear the figure
```

Setting font of the axis and text
```
set(0,'defaultAxesFontName', 'Times')
set(0,'defaultTextFontName', 'Times')
```

Setting font size and weight of the axis labels
```
handle_axis = get(gca, 'Xlabel');
set(handle_axis, 'FontSize', 10, 'FontWeight', 'bold')
handle_axis = get(gca, 'Ylabel');
set(handle_axis, 'FontSize', 10, 'FontWeight', 'bold')
```


Tags that can be used with `plot`
```
'Color', color_name{1}
'LineStyle', line_style{1}
'LineWidth', 1.5
'Marker', marker_style{1} 
'MarkerEdgeColor', color_name{1}
'MarkerFaceColor', [0.5,0.5,0.5]
'MarkerSize', 8
``` 
Adding latex equations
```
eqtext = '$$F_n={1 \over \sqrt{5}}';
eqtext = [eqtext '\left[\left({1+\sqrt{5}\over 2}\right)^n -'];
eqtext = [eqtext '\left({1-\sqrt{5}\over 2}\right)^n\right]$$'];

text(1, 5, eqtext, 'Interpreter', 'Latex', 'FontSize', 12, 'Color', 'k')
```

Split figures
```
%% subplots with a main title and separate titles

suptitle('Main title')

subplot(2,2,1)
plot(x_data, y_data,'-r'), grid on, title('subplot1'),legend('Simulated'), xlabel('X'), ylabel('Y')

subplot(2,2,2)
plot(x_data, y_data,'-g'), grid on, title('subplot2'),legend('Simulated'), xlabel('X'), ylabel('Y')

subplot(2,2,3)
plot(x_data, y_data,'-b'), grid on, title('subplot3'),legend('Simulated'), xlabel('X'), ylabel('Y')

subplot(2,2,4)
plot(x_data, y_data,'-k'), grid on, title('subplot4'),legend('Simulated'), xlabel('X'), ylabel('Y')
```

Two Y axis
```
yyaxis left
plot(x_data,y_data,'-r')

yyaxis right
plot(x_data,10-y_data,'-g')
```
Axis limits
```
ylim([-10 10])
```
Exporting figure for publication
```
export_fig('-transparent','untitled.pdf')
```